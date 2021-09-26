---
title: Kanonische PidTagRecipientType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c3fa109ecb978ab60bad8aa35823bcab65ac986
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599607"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Kanonische PidTagRecipientType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Empfängertyp für einen Nachrichtenempfänger.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Kennung:  <br/> |0x0C15  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der in dieser Eigenschaft enthaltene Empfängertyp besteht aus einem erforderlichen Wert und einem optionalen Flag.
  
Diese Eigenschaft muss genau einen der folgenden Werte enthalten:
  
MAPI_TO 
  
> Der Empfänger ist ein primärer (An)-Empfänger. Clients sind erforderlich, um primäre Empfänger zu verarbeiten. Alle anderen Typen sind optional.
    
MAPI_CC 
  
> Der Empfänger ist ein Cc-Empfänger (Carbon Copy), ein Empfänger, der zusätzlich zu den primären Empfängern eine Nachricht empfängt.
    
MAPI_BCC 
  
> Der Empfänger ist ein BCC-Empfänger (Blind Carbon Copy). Primäre und Kopierempfänger wissen nicht, dass BCC-Empfänger vorhanden sind. 
    
MAPI_P1 
  
> Der Empfänger hat die Nachricht beim vorherigen Versuch nicht erfolgreich empfangen. Dies ist ein erneutes Senden einer früheren Übertragung.
    
Darüber hinaus kann das folgende Kennzeichen festgelegt werden:
  
MAPI_SUBMITTED 
  
> Der Empfänger hat die Nachricht bereits empfangen und muss sie nicht erneut empfangen. Dies ist ein erneutes Senden einer früheren Übertragung. Dieses Flag wird in Verbindung mit den Werten **MAPI_TO,** **MAPI_CC** und **MAPI_BCC** festgelegt. 
    
Der MAPI_P1-Wert und das **flag MAPI_SUBMITTED** werden verwendet, wenn eine Nachricht aufgrund einer Nichtübermittlung an einen oder mehrere der vorgesehenen Empfänger erneut gesendet wird. Für diese erneute Übermittlung legt der Client **MAPI_SUBMITTED** für jeden Empfänger fest, der die Nachricht nicht erneut benötigt, sondern in der Empfängerliste angezeigt werden sollte. Für jeden Empfänger, der die Nachricht zuvor nicht erhalten hat, behält der Client den ursprünglichen Empfänger mit seinem **PR_RECIPIENT_TYPE** Wert unverändert bei, sendet aber zusätzlich eine Kopie des Empfängers mit MAPI_P1 anstelle des ursprünglichen Werts. Diese Kopie, die vor der tatsächlichen Zustellung verworfen wird, erzwingt den Empfänger in den P1-Umschlag und garantiert eine physische erneute Übermittlung an diesen Empfänger. Die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) ist für MAPI_P1 Empfänger auf FALSE festgelegt.
  
Wenn ein Client ein erneutes Senden eines Formulars anzeigt, sind nur die MAPI_P1 Empfänger sichtbar. Wenn der Benutzer keine weiteren Empfänger eingibt, wird die Empfängerliste beim Zugestellten genau so angezeigt wie beim ersten Senden der Nachricht. 
  
Die Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) beziehen sich auf den Empfängertyp. Wenn ein Client die **IMAPIProp::SaveChanges** einer Nachricht aufruft und mindestens ein Empfänger in der Empfängerliste vorhanden ist, legt der Nachrichtenspeicheranbieter diese Eigenschaften wie folgt fest: 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_TO** Empfänger sind.  <br/> |
|PR_DISPLAY_CC  <br/> |Auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_CC** Empfänger sind.  <br/> |
| PR_DISPLAY_BCC  <br/> |Auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_BCC** Empfänger sind.  <br/> |
   
In X.400 sind der P1- oder Zustellungsumschlag die Informationen, die zum Übermitteln einer Nachricht erforderlich sind, einschließlich der Adresseigenschaften des Empfängers und aller Optionsflags, die die Zustellung und Antworten steuern. Der P2- oder Anzeigeumschlag sind die Informationen, die in der Regel für jeden anderen Empfänger als den Nachrichtentext selbst angezeigt werden. Es umfasst in der Regel den Betreff, die Wichtigkeit, die Priorität, die Vertraulichkeit und die Übermittlungszeit sowie die primären und kopierten Empfängernamen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagRecipientStatus (kanonische Eigenschaft)](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo (kanonische Eigenschaft)](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc (kanonische Eigenschaft)](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc (kanonische Eigenschaft)](pidtagdisplaycc-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

