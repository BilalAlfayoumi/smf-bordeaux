# Configuration EmailJS – nouveaux champs Contact + template email stylé

## Variables à mapper dans EmailJS

Le site envoie ces variables :

- `from_name`
- `from_first_name`
- `from_last_name`
- `from_email`
- `phone`
- `age_group`
- `message`
- `reply_to`

Compatibilité incluse avec anciens noms :
`user_name`, `user_first_name`, `user_last_name`, `user_email`, `user_phone`.

## Sujet recommandé

```txt
[Nouvelle demande SMF Bordeaux] {{from_first_name}} {{from_last_name}} — {{age_group}}
```

## Template HTML recommandé (EmailJS)

```html
<div style="margin:0;padding:0;background:#f4f6f8;font-family:Arial,Helvetica,sans-serif;color:#1f2937;">
  <table role="presentation" width="100%" cellspacing="0" cellpadding="0" style="background:#f4f6f8;padding:24px 12px;">
    <tr><td align="center">
      <table role="presentation" width="100%" cellspacing="0" cellpadding="0" style="max-width:680px;background:#ffffff;border:1px solid #e5e7eb;border-radius:12px;overflow:hidden;">
        <tr><td style="background:#0f766e;padding:20px 24px;color:#ffffff;">
          <h1 style="margin:0;font-size:20px;">Nouvelle demande de contact</h1>
          <p style="margin:6px 0 0 0;font-size:13px;">Site SMF Bordeaux</p>
        </td></tr>

        <tr><td style="padding:20px 24px 8px 24px;"><h2 style="margin:0;font-size:16px;">Informations du contact</h2></td></tr>
        <tr><td style="padding:0 24px 20px 24px;">
          <table role="presentation" width="100%" cellspacing="0" cellpadding="0" style="border-collapse:collapse;">
            <tr><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;width:38%;"><strong>Prénom</strong></td><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;">{{from_first_name}}</td></tr>
            <tr><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;"><strong>Nom</strong></td><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;">{{from_last_name}}</td></tr>
            <tr><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;"><strong>Email</strong></td><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;"><a href="mailto:{{from_email}}">{{from_email}}</a></td></tr>
            <tr><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;"><strong>Téléphone</strong></td><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;">{{phone}}</td></tr>
            <tr><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;"><strong>Tranche d'âge</strong></td><td style="padding:10px 0;border-bottom:1px solid #e5e7eb;">{{age_group}}</td></tr>
          </table>
        </td></tr>

        <tr><td style="padding:0 24px 8px 24px;"><h2 style="margin:0;font-size:16px;">Message</h2></td></tr>
        <tr><td style="padding:0 24px 24px 24px;"><div style="background:#f9fafb;border:1px solid #e5e7eb;border-radius:8px;padding:14px;white-space:pre-wrap;">{{message}}</div></td></tr>
        <tr><td style="padding:0 24px 24px 24px;"><a href="mailto:{{reply_to}}" style="display:inline-block;background:#0f766e;color:#fff;text-decoration:none;padding:11px 16px;border-radius:8px;">Répondre</a></td></tr>
      </table>
    </td></tr>
  </table>
</div>
```

## Étapes dashboard

1. Ouvrir EmailJS > **Email Templates**
2. Ouvrir `template_39nzsbp`
3. Remplacer le sujet
4. Remplacer le contenu HTML
5. Sauvegarder
6. Tester via le formulaire web

## IDs utilisés côté code

- Service: `service_ubi0bue`
- Template: `template_39nzsbp`
- Public key: `R8lXCtn2Vc6Dy3A0D`
