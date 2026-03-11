---
layout: presentation
title: "Introduction to GDPR for Developers and Testers"
date: 2024-05-17 10:00:00 +0530
author: anandhu
image: /imgs/presentation/gdpr/hero_engineering.png
permalink: /article/intro-to-gdpr-for-engineers.html
---

<section class="slide slide--intro" style="background-image: url('{{ page.image | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h1 class="slide-title">Introduction to GDPR for Developers and Testers</h1>
        <p class="slide-subtitle">Building Privacy-First Systems via Engineering Excellence</p>
        <p>Presenter: Anandhu Krishnan</p>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/data_protection_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Why Engineers Must Care</h2>
        <p class="slide-subtitle">GDPR is a technical responsibility, not just a legal one.</p>
        <ul class="slide-points">
            <li>Secure storage and minimal collection.</li>
            <li>Enable data access and deletion.</li>
            <li>Privacy-by-design architecture.</li>
        </ul>
        <div class="slide-impact">Penalties: Up to €20 million or 4% of annual global turnover.</div>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/personal_data_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Special Categories of Data</h2>
        <p class="slide-subtitle">Sensitive data requires stronger protection.</p>
        <ul class="slide-points">
            <li>Health & Biometric data</li>
            <li>Political opinions & Religious beliefs</li>
            <li>Genetic data</li>
        </ul>
        <p>Applications must avoid collecting these unless absolutely required.</p>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/security_arch_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Core GDPR Principles</h2>
        <ul class="slide-points">
            <li>Lawfulness, Fairness, Transparency</li>
            <li>Purpose & Storage Limitation</li>
            <li>Data Minimization & Accuracy</li>
            <li>Integrity, Confidentiality & Accountability</li>
        </ul>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/security_arch_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Privacy by Design</h2>
        <p class="slide-subtitle">Built-in, not bolted-on.</p>
        <ul class="slide-points">
            <li>Minimal data collection and secure storage.</li>
            <li>Role-based access control (RBAC).</li>
            <li>Data encryption and comprehensive audit logging.</li>
        </ul>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/data_protection_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">User Right to Access Data</h2>
        <ul class="slide-points">
            <li>Users can request what data is stored and why.</li>
            <li>Users can request how it is used.</li>
        </ul>
        <div class="slide-code">
            <p>Example Implementation:</p>
            <code>GET /user/data-export</code>
        </div>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/data_protection_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Right to Erasure (Be Forgotten)</h2>
        <ul class="slide-points">
            <li>Users can request deletion of their personal data.</li>
            <li>Remove from databases, logs, and backups where possible.</li>
        </ul>
        <div class="slide-code">
            <p>Example Implementation:</p>
            <code>DELETE /user/account</code>
        </div>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/checklist_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Data Retention Policies</h2>
        <table class="slide-table">
            <thead>
                <tr>
                    <th>Data Type</th>
                    <th>Retention Period</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>User Account</td>
                    <td>Until account deletion</td>
                </tr>
                <tr>
                    <td>Logs</td>
                    <td>90 days</td>
                </tr>
                <tr>
                    <td>Security Logs</td>
                    <td>1 year</td>
                </tr>
            </tbody>
        </table>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/security_arch_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Logging Without Violating GDPR</h2>
        <div class="slide-grid">
            <div class="grid-item">
                <h3 style="color: #ff4d4d;">Bad Practice</h3>
                <p>Login failed for user: john@email.com</p>
                <p>Password: mypassword123</p>
            </div>
            <div class="grid-item">
                <h3 style="color: #4dff4d;">Good Practice</h3>
                <p>Login failed for user ID: 49283</p>
                <p>Source IP logged separately.</p>
            </div>
        </div>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/checklist_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Role of QA Engineers</h2>
        <ul class="slide-points">
            <li>Test data encryption and access controls.</li>
            <li>Verify deletion and consent flows.</li>
            <li>Verify data export functionality.</li>
            <li>Security testing for PII leakage.</li>
        </ul>
    </div>
</section>

<section class="slide" style="background-image: url('{{ '/imgs/presentation/gdpr/data_protection_bg.png' | relative_url }}');">
    <div class="slide--overlay"></div>
    <div class="slide-content">
        <h2 class="slide-title">Final Recommendations</h2>
        <ul class="slide-points">
            <li>Design privacy at the architecture level.</li>
            <li>Implement strong data security (TLS, AES).</li>
            <li>Allow user control of personal data.</li>
            <li>Continuously test privacy features.</li>
        </ul>
        <div class="slide-key-idea">Privacy is a shared responsibility.</div>
    </div>
</section>
