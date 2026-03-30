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
