# 🔐 Como Configurar o reCAPTCHA Invisível no Drupal

Este guia explica como proteger formulários do Drupal com o **reCAPTCHA Invisível (v2)** ou **reCAPTCHA v3** usando os módulos CAPTCHA e reCAPTCHA.

---

## ✅ Pré-requisitos

- Drupal 9 ou superior instalado.
- Acesso administrativo ao site Drupal.
- Conta no Google reCAPTCHA: https://www.google.com/recaptcha/admin

---

## 📦 Módulos Necessários

- [CAPTCHA](https://www.drupal.org/project/captcha)
- [reCAPTCHA](https://www.drupal.org/project/recaptcha)

Instale via Composer:

```bash
composer require drupal/captcha drupal/recaptcha
```

Ative os módulos:

```bash
drush en captcha recaptcha
```

---

## 🔧 Obtenha as Chaves do Google reCAPTCHA

1. Acesse: https://www.google.com/recaptcha/admin/create
2. Registre seu site e selecione:
   - **reCAPTCHA v2** > “Invisible reCAPTCHA badge” _ou_
   - **reCAPTCHA v3**
3. Copie a **chave do site** e a **chave secreta**

---

## ⚙️ Configuração no Drupal

### 1. Configurar o CAPTCHA

Acesse:
```
Administração > Configuração > Pessoas > CAPTCHA
```
- Escolha os formulários onde o CAPTCHA será aplicado (login, registro, contato...)
- Em **Tipo de desafio**, selecione `reCAPTCHA`

### 2. Configurar o reCAPTCHA

Acesse:
```
Administração > Configuração > Pessoas > reCAPTCHA
```
- Insira as **chaves** do Google
- Escolha o tipo de reCAPTCHA (v2 invisível ou v3)
- Marque **“Usar o reCAPTCHA invisível”**
- Personalize o tema, posição do badge e mensagens conforme sua necessidade

---

## 🧪 Teste

Acesse um dos formulários protegidos.

- O CAPTCHA será **invisível** — apenas a badge do Google aparecerá discretamente (v2), ou nada (v3).
- Teste o envio para validar a integração.

---

## 💡 Dicas Extras

- Para reforçar a segurança sem afetar a UX, use também o módulo [AntiBot](https://www.drupal.org/project/antibot)
- No reCAPTCHA v3, defina o score mínimo de confiança para bloquear bots silenciosamente.

---

## 📌 Conclusão

Usar o reCAPTCHA invisível melhora a segurança do seu site **sem impactar a experiência do usuário**, sendo uma solução recomendada para formulários em produção.

Se quiser mais tutoriais práticos como esse, acompanhe meu repositório no GitHub! 😉

