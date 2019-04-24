---
title: Eigenschaften (Account Management API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: In diesem Abschnitt werden die Eigenschaften in der Account Management-API beschrieben.
ms.openlocfilehash: d0b8c06716bd2f3a3bb2941e098bd9f11ab87183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326439"
---
# <a name="properties-account-management-api"></a>Eigenschaften (Account Management API)

In diesem Abschnitt werden die Eigenschaften in der Account Management-API beschrieben.
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Dies ist das sekundäre Konto "Send"-Stempel für die Nachricht.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Dies ist das primäre Konto "Send"-Stempel für eine Nachricht.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Stellt die Eintrags-ID des Standard Zustellungs Ordners für das Konto dar.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Stellt die Eintrags-ID des Standard Zustellungs Speichers für das Konto dar.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Gibt einen Bezeichner zurück, der ein Konto innerhalb des Profils eindeutig identifiziert, in dem das Konto erstellt wird.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, wenn das Konto ein Exchange-Konto ist.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Gibt eine Konto-ID zurück, die in Outlook-Profilen eindeutig ist.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Gibt den Kontonamen zurück oder legt ihn fest.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Ruft den eindeutigen Bezeichner (UID) für den Profil Abschnitt ab, in dem die Kontoeinstellungen gespeichert werden.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Gibt das Konto "Send"-Stempel zurück.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Stellt die Eintrags-ID des Standardordners für gesendete Elemente für das Konto dar.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Gibt den Konto Stempel zurück.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Gibt die e-Mail-Adresse für das Konto an.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Gibt den Anzeigenamen des Benutzers zurück oder legt ihn fest.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Stellt das Benutzerkennwort für ein allgemeines Internet Postfach dar.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Stellt die Nummer des Anschlusses für ein allgemeines Internet Postfach dar.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Stellt den Servernamen eines allgemeinen Internet Postfachs dar.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Gibt an, ob Secure Socket Layer (SSL) für ein allgemeines Internet Postfach verwendet werden soll.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Gibt an, ob die Secure Password Authentication (SPA) für ein allgemeines Internet Postfach verwendet werden soll.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Stellt den Benutzernamen für ein allgemeines Internet Postfach dar.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Stellt eine [ACCT_BIN](acct_bin.md) -Struktur dar, die die UID eines Exchange-Kontos enthält.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Ruft die Adressbucheintrags-ID für das Konto ab oder legt Sie fest.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Stellt Transporteinstellungen dar, die Outlook zum Ermitteln der erforderlichen Synchronisierungsaufgaben verwendet, und zum Deaktivieren der Benutzeroberflächenelemente, die das Konto nicht unterstützt.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Gibt an, dass eine Kopie einer Nachricht auf dem Server für ein POP-Konto hinterlassen werden soll.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Gibt die Authentifizierungsmethode für das SMTP-Konto an.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Stellt das Kennwort des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Stellt die Nummer des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Stellt den Servernamen des SMTP-Kontos dar.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Gibt an, ob das SSL-Protokoll (Secure Socket Layer) für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Gibt an, ob die Authentifizierung für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Gibt an, ob die Secure Password Authentication (SPA) für das SMTP-Konto verwendet werden soll.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Stellt den Benutzernamen für das SMTP-Konto dar.  <br/> |
   

