<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>李妤 - 字节跳动外派运营</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        }
        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        .card {
            max-width: 480px;
            width: 100%;
            background: #ffffff;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            position: relative;
        }
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 6px;
            background: linear-gradient(90deg, #0066ff 0%, #00ccff 100%);
        }
        .header {
            background: linear-gradient(135deg, #0066ff 0%, #00ccff 100%);
            padding: 40px 30px 30px;
            color: white;
            text-align: center;
            position: relative;
        }
        .logo-container {
            width: 80px;
            height: 80px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            border: 3px solid rgba(255, 255, 255, 0.3);
        }
        .logo {
            font-size: 32px;
            font-weight: bold;
            color: white;
        }
        .title h1 {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 8px;
            letter-spacing: 0.5px;
        }
        .title p {
            font-size: 14px;
            opacity: 0.9;
            font-weight: 400;
        }
        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            margin-top: 10px;
            font-weight: 500;
        }
        .content {
            padding: 30px;
        }
        .info-list {
            list-style: none;
        }
        .info-item {
            display: flex;
            align-items: center;
            padding: 16px 0;
            border-bottom: 1px solid #f0f0f0;
        }
        .info-item:last-child {
            border-bottom: none;
        }
        .label {
            width: 100px;
            color: #666;
            font-weight: 500;
            font-size: 14px;
            display: flex;
            align-items: center;
        }
        .label::before {
            content: '•';
            color: #0066ff;
            margin-right: 8px;
            font-size: 18px;
        }
        .value {
            color: #1a1a1a;
            flex: 1;
            font-size: 16px;
            font-weight: 500;
        }
        .highlight {
            color: #0066ff;
            font-weight: 600;
        }
        .status-indicator {
            display: inline-flex;
            align-items: center;
            padding: 4px 12px;
            background: #e6f7ff;
            color: #0066ff;
            border-radius: 16px;
            font-size: 12px;
            font-weight: 500;
            margin-left: 8px;
        }
        .status-indicator::before {
            content: '';
            width: 6px;
            height: 6px;
            background: #0066ff;
            border-radius: 50%;
            margin-right: 6px;
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { opacity: 0.6; }
            50% { opacity: 1; }
            100% { opacity: 0.6; }
        }
        .footer {
            background: #f8f9fa;
            padding: 20px 30px;
            text-align: center;
            border-top: 1px solid #e9ecef;
        }
        .footer p {
            color: #666;
            font-size: 12px;
            line-height: 1.5;
        }
        .footer .copyright {
            color: #999;
            font-size: 11px;
            margin-top: 8px;
        }
        .byte-logo {
            display: inline-block;
            font-weight: bold;
            color: #0066ff;
            position: relative;
        }
        .byte-logo::after {
            content: '跳动';
            color: #ff4d4f;
            margin-left: 2px;
        }
        /* 人像区域样式（优化显示兼容性） */
        .avatar-section {
            text-align: center;
            padding: 20px 30px 30px;
            border-top: 1px dashed #e9ecef;
            margin-top: 20px;
        }
        .avatar-title {
            color: #666;
            font-size: 14px;
            margin-bottom: 15px;
            font-weight: 500;
        }
        .avatar-container {
            width: 160px;
            height: 200px;
            background: #f8f9fa;
            border: 2px solid #0066ff; /* 字节品牌蓝边框 */
            border-radius: 12px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        .avatar {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block; /* 解决图片底部间隙问题 */
        }
        /* 图片加载失败时显示备用文本 */
        .avatar-container::after {
            content: '证件照';
            color: #999;
            font-size: 14px;
        }
        @media (max-width: 480px) {
            .card {
                border-radius: 16px;
            }
            .header {
                padding: 30px 20px 25px;
            }
            .content {
                padding: 20px;
            }
            .info-item {
                padding: 14px 0;
            }
            .label {
                width: 90px;
                font-size: 13px;
            }
            .value {
                font-size: 15px;
            }
            .avatar-container {
                width: 140px;
                height: 180px;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="header">
            <div class="logo-container">
                <div class="logo">字</div>
            </div>
            <div class="title">
                <h1>临时到访人员信息</h1>
                <p>ByteDance Temporary Visitor Information</p>
                <div class="badge">阿里外派 - 活动策划</div>
            </div>
        </div>
        
        <div class="content">
            <ul class="info-list">
                <li class="info-item">
                    <span class="label">姓名</span>
                    <span class="value highlight">李妤</span>
                </li>
                <li class="info-item">
                    <span class="label">职位</span>
                    <span class="value">运营专员 <span class="status-indicator">外派</span></span>
                </li>
                <li class="info-item">
                    <span class="label">到访原因</span>
                    <span class="value">阿里员工外派 - 活动策划</span>
                </li>
                <li class="info-item">
                    <span class="label">有效期</span>
                    <span class="value">30天（激活后生效）</span>
                </li>
                <li class="info-item">
                    <span class="label">接待部门</span>
                    <span class="value">市场部 - 调研部</span>
                </li>
                <li class="info-item">
                    <span class="label">员工编号</span>
                    <span class="value">BD-OP-2025-0876</span>
                </li>
                <li class="info-item">
                    <span class="label">访问权限</span>
                    <span class="value">办公区、会议室、员工餐厅</span>
                </li>
            </ul>
            
            <!-- 人像区域（优化图片引用，确保显示） -->
            <div class="avatar-section">
                <div class="avatar-title">人员证件照</div>
                <div class="avatar-container">
                    <!-- 替换后的图片链接 -->
                    <img src="https://douyin-rpg.github.io/picx-images-hosting/photo_2025-12-28_11-12-48.4xv0j09r9a.webp" alt="李妤证件照" class="avatar" onerror="this.style.display='none'">
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>本信息仅用于<span class="byte-logo">字节</span>园区临时通行核验</p>
            <p class="copyright">© 2025 ByteDance Inc. 保留所有权利 | 信息安全级别：内部使用</p>
        </div>
    </div>
</body>
</html>
