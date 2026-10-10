# 只言片语 · ZhiYanPianYu

面向 AI 短片创作的本地工作台，围绕剧本、角色与场景、分镜、参考图、视频生成、后期拼接组织创作流程。基于 [VideoClaw / FilmAgent 上游仓库](https://github.com/HITsz-TMG/VideoClaw)的应用代码整理，保留原有版权声明。

**当前状态：可运行的演示项目。已验证前后端启动和真实单片段生成。**

## 真实生成样片

“雨夜城市街道，镜头缓慢向前”，2026-10-08 实际调用生成。

[播放 / 下载 5 秒样片](docs/demo/rain-night-5s.mp4)

![视频采样帧](docs/demo/frames-check.png)

- 首帧：`wan2.7-image`；视频：`wan2.6-i2v`。
- 视频轨道 5.000 秒，1280 × 720，30 fps，H.264；包含 AAC 音轨，容器时长约 5.008 秒。
- 完整 FFmpeg 解码通过。生成约耗时 151 秒，含首帧。
- 采样帧可见街道透视与行人运动；夜景氛围比预期明亮。
- 标价估算为 0.20 元首帧 + 5 × 0.60 元视频 = 3.20 元；不是账户实际账单，免费额度未核实。

这条样片直接使用项目的 `ImageClient` 和 `VideoClient`，验证的是单片段生成，不代表六阶段工作流已全部通过。

## 许可与来源

应用来源：[HITsz-TMG/VideoClaw](https://github.com/HITsz-TMG/VideoClaw)（原 FilmAgent 仓库地址现重定向至此）。保留原项目中的 Innate Labs 等署名；这些署名属于上游来源，不表示该仓库全部由当前仓库拥有者原创。

[MIT License](LICENSE) · [上游 MIT 许可原文](licenses/VideoClaw-MIT.txt)。外部 API、模型及素材的使用受各提供方相应条款约束。

## 设计思路

- 定位：数字人 2.0 · AI Film Studio（V2.0 · BUILDING）
- 一句话：1.0 验证成功后立项：从单点口播升级为覆盖剧本、角色、分镜、参考图到视频的 AI 短片创作工作台。

---
本仓库仅用于展示，不含源码。更多作品见 [作品集](https://freya-qian.github.io/)。
