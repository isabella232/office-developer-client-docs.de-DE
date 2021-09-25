---
title: Eigenschaften (Account Management API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: In diesem Abschnitt werden die Eigenschaften in der Kontoverwaltungs-API beschrieben.
ms.openlocfilehash: b3c7a739234b290d0a032f202a13f663912b7009
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572200"
---
# <a name="properties-account-management-api"></a>Eigenschaften (Account Management API)

In diesem Abschnitt werden die Eigenschaften in der Kontoverwaltungs-API beschrieben.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Dies ist der sekundäre "Senden"-Stempel des Kontos für die Nachricht.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Dies ist der primäre Kontostempel "Senden" für eine Nachricht.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsordners für das Konto dar.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Stellt die Eintrags-ID des Standardzustellungsspeichers für das Konto dar.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, Wenn das Konto ein Exchange Konto ist.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Gibt einen Kontobezeichner zurück, der für Outlook Profile eindeutig ist.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Gibt den Kontonamen zurück oder legt den Kontonamen fest.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Ruft den eindeutigen Bezeichner (UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Gibt den Stempel "Senden" des Kontos zurück.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Gibt den Kontostempel zurück.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Gibt die E-Mail-Adresse für das Konto an.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Gibt den Anzeigenamen des Benutzers zurück oder legt den Namen fest.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Stellt das Benutzerkennwort für ein allgemeines Internetpostfach dar.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Stellt die Portnummer für ein allgemeines Internetpostfach dar.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Stellt den Servernamen eines allgemeinen Internetpostfachs dar.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Gibt an, ob SSL (Secure Socket Layer) für ein allgemeines Internetpostfach verwendet werden soll.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Gibt an, ob die sichere Kennwortauthentifizierung (Secure Password Authentication, SPA) für ein allgemeines Internetpostfach verwendet werden soll.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Stellt den Benutzernamen für ein allgemeines Internetpostfach dar.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Stellt eine [ACCT_BIN](acct_bin.md) Struktur dar, die die UID eines Exchange Kontos enthält.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Ruft die Adressbucheintrags-ID für das Konto ab oder legt sie fest.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Stellt Transporteinstellungen dar, die Outlook verwendet, um die erforderlichen Synchronisierungsaufgaben zu ermitteln und die Benutzeroberflächenelemente zu deaktivieren, die das Konto nicht unterstützt.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Gibt an, dass eine Kopie einer Nachricht für ein POP-Konto auf dem Server verbleibt.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Gibt die Authentifizierungsmethode an, die für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Stellt das Kennwort des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Stellt die Portnummer des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Stellt den Servernamen des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Gibt an, ob das SSL-Protokoll (Secure Socket Layer) für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Gibt an, ob die Authentifizierung für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Gibt an, ob die sichere Kennwortauthentifizierung (Secure Password Authentication, SPA) für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Stellt den Benutzernamen für das SMTP-Konto dar.  <br/> |
   

