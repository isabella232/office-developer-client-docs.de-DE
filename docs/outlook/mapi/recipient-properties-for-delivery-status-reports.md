---
title: Empfängereigenschaften für Übermittlungsstatusberichte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 58711a18fa6dc512cca10644437bee2ecd4d2143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592997"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Empfängereigenschaften für Übermittlungsstatusberichte

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die folgenden Eigenschaften sind für die Übermittlung von Statusberichten für Empfänger vorhanden. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) wird nicht auf Unzustellbarkeitsberichte verwendet. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) und **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) werden nur für Unzustellbarkeitsberichte verwendet.
  
**Titel der Tabelle**

|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Enthält Datum und Uhrzeit, an dem die ursprüngliche Nachricht übermittelt wurde.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Enthält eine MAPI-Eintrags-ID, die zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts verwendet.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Enthält einen diagnostic Code, der Teil der non-Delivery Report bildet.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Enthält eine Textzeichenfolge, die die Absender benutzerdefinierte Nachrichtenklasse wie IPM identifiziert. Beachten Sie.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Enthält einen codierten Grund für ein Unzustellbarkeitsbericht, die Teil der non-Delivery Report bildet.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Enthält den ursprünglichen Anzeigenamen für einen Eintrag aus einem Adressbuch in ein persönliches Adressbuch oder anderen beschreibbaren des Adressbuchs kopiert.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Enthält die ursprünglichen Eintrags-ID für einen Eintrag aus einem Adressbuch an ein persönliches Adressbuch oder anderen beschreibbaren Adressbuch kopiert.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Enthält den ursprünglichen Suche Schlüssel für einen Eintrag aus einem Adressbuch an ein persönliches Adressbuch oder anderen beschreibbaren Adressbuch kopiert.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Enthält den Empfängertyp für einen Nachrichtenempfänger.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Optionalen Text für einen Bericht generiert, die für die messaging-System enthält.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Enthält Datum und Uhrzeit, wann das messaging-System ein Bericht erstellt.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Enthält einen binären vergleichbaren Schlüssel, der für eine Suche korrelierte Objekte identifiziert.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Enthält einen Wert zum Verknüpfen eines Symbols mit einer bestimmten Zeile einer Tabelle verwendet.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Enthält den Typ eines Objekts.  <br/> |
   

