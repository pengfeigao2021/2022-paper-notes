## Ransac

ransac 试图解决一个新的问题：全部数据中有很大比例的outlier，传统的Least Square方式不适合全量数据fit。

Ransac把误差分为两种，classification error和measurement error。
measurement error服从高斯分布，所以全局平滑对减小这部分error有用。
classification error代表选错feature。这部分误差影响全局模型的性能。

## Papers

1. Martin A. Fischler and Robert C. Bolles. “Random sample consensus: a paradigm for model fitting with applications to image analysis and automated cartography” Communications of The ACM (1981): n. pag.