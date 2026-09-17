# opencv-novs — pattern_matching module

OpenCV extra module with industrial template matching, ported from [OpenCvSharp](https://github.com/newocean-group/OpenCvSharp) `OpenCvSharpExtern`.

## Matchers

| File | Algorithm |
|------|-----------|
| `fast_ncc_matcher.*` | Pyramid NCC |
| `match_tool_ncc_matcher.*` | MatchTool-style NCC |
| `shape_based_matcher.*` | Halcon-style shape matching (~5.5k lines) |

## Python API (via opencv-novs-python)

```python
import cv2
m = cv2.pattern_matching.ShapeBasedMatcher_create()
```

Build parent repo [opencv-novs-python](https://github.com/newocean-group/opencv-novs-python) with `ENABLE_CONTRIB=1`.

## Sync from OpenCvSharp

From the parent repo root:

```powershell
.\scripts\sync_from_opencvsharp.ps1
cd pattern_matching
git commit -am "sync from OpenCvSharp"
git push
```

## License

MIT (see `LICENSE.txt`). Native matching code follows New Ocean / OpenCvSharp project terms.
