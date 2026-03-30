# Mini-Humanoid Cloth Folding Roadmap (arXiv-aligned — March 2026)

## Priority 1: Semantic Keypoints (CLASP-inspired)
- Detect language-described keypoints ("collar", "sleeve", "hem") from RGB-D or simulation images
- Use them to guide grasp and fold points instead of pure geometric methods

## Priority 2: Closed-Loop Policy (FoldNet-inspired)
- Add keypoint error detection + recovery during folding sequences
- Hook into Unitree dataset loader

## Priority 3: LLM + Keypoints Integration
- Let LLM plan folding steps using detected semantic keypoints
- Extend current multi-task bash infrastructure

Once implemented, test on simulated 1ft android laundry tasks.

## Progress — March 30 2026
**Added:** `vision/semantic_keypoints.py` — CLASP-style semantic keypoint detector (collar, sleeves, shoulders, hem).

**Next immediate steps:**
1. Integrate with Unitree UnifoLM-WBT dataset loader (load RGB-D frames)
2. Replace heuristic detection with lightweight keypoint model (inspired by FoldNet)
3. Add closed-loop correction (if fold fails → re-detect keypoints)
4. Hook into multi-task folding planner (LLM → semantic keypoint commands)

Run with: `python -m vision.semantic_keypoints`
