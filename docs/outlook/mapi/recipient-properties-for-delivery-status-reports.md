---
title: Empfänger Eigenschaften für zuStellungs Status Berichte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 784cac21aac5de18952f3768af9b8f189f604981
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328434"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Empfänger Eigenschaften für zuStellungs Status Berichte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die folgenden Eigenschaften sind für Zustellungsstatus Berichte für Empfänger vorhanden. **PR_DELIVER_TIME** ([Pidtagdelivertime (](pidtagdelivertime-canonical-property.md)) wird nicht für Unzustellbarkeitsberichte verwendet. **PR_NDR_DIAG_CODE** ([Pidtagnondeliveryreportdiagcode (](pidtagnondeliveryreportdiagcode-canonical-property.md)) und **PR_NDR_REASON_CODE** ([pidtagnondeliveryreportreasoncode (](pidtagnondeliveryreportreasoncode-canonical-property.md)) werden nur für Unzustellbarkeitsberichte verwendet.
  
**Tabellentitel**

|**Eigenschaft**|**Decription**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([Pidtagdelivertime (](pidtagdelivertime-canonical-property.md))  <br/> |Enthält das Datum und die Uhrzeit, zu der die ursprüngliche Nachricht zugestellt wurde.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Enthält eine MAPI-Eintrags-ID zum Öffnen und Bearbeiten der Eigenschaften eines bestimmten MAPI-Objekts.  <br/> |
|**PR_NDR_DIAG_CODE** ([Pidtagnondeliveryreportdiagcode (](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Enthält einen Diagnosecode, der Teil eines Unzustellbarkeitsberichts ist.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Enthält eine Textzeichenfolge, die die Absender definierte Nachrichtenklasse identifiziert, beispielsweise IPM. Hinweis.  <br/> |
|**PR_NDR_REASON_CODE** ([Pidtagnondeliveryreportreasoncode (](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Enthält einen codierten Grund für die Nichtlieferung, der Teil eines Unzustellbarkeitsberichts ist.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([Pidtagoriginaldisplayname (](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Enthält den ursprünglichen Anzeigenamen für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([Pidtagoriginalentryid (](pidtagoriginalentryid-canonical-property.md))  <br/> |Enthält die ursprüngliche Eintrags-ID für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([Pidtagoriginalsearchkey (](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Enthält den ursprünglichen Suchschlüssel für einen Eintrag, der aus einem Adressbuch in ein persönliches Adressbuch oder ein anderes beschreibbares Adressbuch kopiert wurde.  <br/> |
|**PR_RECIPIENT_TYPE** ([Pidtagrecipienttype (](pidtagrecipienttype-canonical-property.md))  <br/> |Enthält den Empfängertyp für einen Nachrichtenempfänger.  <br/> |
|**PR_REPORT_TEXT** ([Pidtagreporttext (](pidtagreporttext-canonical-property.md))  <br/> |Enthält optionalen Text für einen vom Messagingsystem generierten Bericht.  <br/> |
|**PR_REPORT_TIME** ([Pidtagreporttime (](pidtagreporttime-canonical-property.md))  <br/> |Enthält das Datum und die Uhrzeit, zu denen das Messagingsystem einen Bericht generiert hat.  <br/> |
|**PR_SEARCH_KEY** ([Pidtagsearchkey (](pidtagsearchkey-canonical-property.md))  <br/> |Enthält einen binären-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Enthält einen Wert, der zum Zuordnen eines Symbols zu einer bestimmten Zeile einer Tabelle verwendet wird.  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |Enthält den Typ eines Objekts.  <br/> |
   

