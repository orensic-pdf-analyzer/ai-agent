# 🧹 AI Swachhata + WhatsApp Agent

છોટાઉદેપુર નગરપાલિકા માટે QR → Complaint → AI Classification → Dashboard સિસ્ટમ.

## 1. Run
Node.js 20+ ઇન્સ્ટોલ કરો.

```bash
npm install
cp .env.example .env
npm start
```
Browser: http://localhost:3000

## 2. મુખ્ય પેજ
- Dashboard: `/`
- Citizen QR complaint: `/report.html?qr=WARD-05`
- QR Generator: `/qr.html`
- WhatsApp webhook: `/webhook/whatsapp`

## 3. WhatsApp Cloud API
`.env` માં Meta WhatsApp Cloud API credentials મૂકો:
- WHATSAPP_VERIFY_TOKEN
- WHATSAPP_ACCESS_TOKEN
- WHATSAPP_PHONE_NUMBER_ID
- WHATSAPP_API_VERSION

Meta developer console માં webhook callback URL તરીકે `https://YOUR-DOMAIN/webhook/whatsapp` અને Verify Token તરીકે `.env` નો token મૂકો.

## 4. AI
હાલ demo classification local rulesથી થાય છે. Productionમાં OPENAI_API_KEY જોડીને Gujarati text + photo classification ઉમેરવા માટે `classify()` function બદલી શકાય.

## 5. Production માટે જરૂરી
- HTTPS domain
- Meta WhatsApp Business account
- Database backup
- Staff login/role permissions
- Photo storage
- GPS validation
- Audit log
- Privacy/retention policy
