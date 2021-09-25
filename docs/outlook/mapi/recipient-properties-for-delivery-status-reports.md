---
title: Empfängereigenschaften für Übermittlungsstatusberichte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1063d1a7a062b8b07d9ff66958efc5e65ef8737e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591311"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Empfängereigenschaften für Übermittlungsstatusberichte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden Eigenschaften sind für Übermittlungsstatusberichte für Empfänger vorhanden. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) wird nicht für Unzustellbarkeitsberichte verwendet. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) und **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) werden nur für Unzustellbarkeitsberichte verwendet.
  
**Tabellentitel**

|**Eigenschaft**|**Dezimierung**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Enthält das Datum und die Uhrzeit, zu der die ursprüngliche Nachricht zugestellt wurde.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Enthält einen MAPI-Eintragsbezeichner, der zum Öffnen und Bearbeiten von Eigenschaften eines bestimmten MAPI-Objekts verwendet wird.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Enthält einen Diagnosecode, der Teil eines Unzustellbarkeitsberichts ist.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Enthält eine Textzeichenfolge, die die vom Absender definierte Nachrichtenklasse identifiziert, z. B. IPM.Note.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Enthält einen codierten Grund für die Unzustellbarkeit, der Teil eines Unzustellbarkeitsberichts ist.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Enthält den ursprünglichen Anzeigenamen für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes schreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Enthält den ursprünglichen Eintragsbezeichner für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Enthält den ursprünglichen Suchschlüssel für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Enthält den Empfängertyp für einen Nachrichtenempfänger.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Enthält optionalen Text für einen vom Messagingsystem generierten Bericht.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Enthält das Datum und die Uhrzeit, zu der das Messagingsystem einen Bericht generiert hat.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Enthält einen mit Binärdaten vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Enthält einen Wert, der zum Zuordnen eines Symbols zu einer bestimmten Zeile einer Tabelle verwendet wird.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Enthält den Typ eines Objekts.  <br/> |
   

