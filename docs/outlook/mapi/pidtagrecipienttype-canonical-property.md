---
title: PidTagRecipientType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ddde5d206eb4be56ce6a7bae77eb00237f12a0f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584296"
---
# <a name="pidtagrecipienttype-canonical-property"></a>PidTagRecipientType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Empfängertyp für einen Nachrichtenempfänger.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Kennung:  <br/> |0x0C15  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der in dieser Eigenschaft enthaltenen Empfängertyp besteht aus ein erforderlicher Wert und eine optionale Kennzeichnung.
  
Diese Eigenschaft muss genau einen der folgenden Werte enthalten:
  
MAPI_TO 
  
> Der Empfänger ist ein primärer (Empfänger To). Clients sind erforderlich, um die primären Empfänger zu behandeln. Alle anderen Typen sind optional.
    
MAPI_CC 
  
> Beim Empfänger handelt es sich um einen Empfänger Carbon Copy, Kopie (CC), einen Empfänger an, die zusätzlich zu den primären Empfänger eine Nachricht empfängt.
    
MAPI_BCC 
  
> Beim Empfänger handelt es sich um einen Empfänger blind Carbon Copy, Blindkopie (BCC). Primäre und Carbon Copy, Blindkopie Empfänger ist wissen das Vorhandensein der BCC-Empfänger. 
    
MAPI_P1 
  
> Der Empfänger nicht die Meldung auf vorherigen Versuch erhalten. Hierbei handelt es sich um eine erneute Senden eines eine frühere Übertragung.
    
Darüber hinaus können die folgenden Kennzeichen festgelegt werden:
  
MAPI_SUBMITTED 
  
> Der Empfänger die Nachricht wurde bereits empfangen und muss nicht erneut empfangen. Hierbei handelt es sich um eine erneute Senden eines eine frühere Übertragung. Dieses Kennzeichen werden in Verbindung mit den Werten **MAPI_TO**, **MAPI_CC**und **MAPI_BCC** festgelegt. 
    
Der Wert MAPI_P1 und das Flag **MAPI_SUBMITTED** werden verwendet, wenn eine Nachricht aufgrund von Nondelivery an einen oder mehrere der angegebenen Empfänger erneut übertragen wird. Für diese erneute Übertragung wird der Client **MAPI_SUBMITTED** auf jeden Empfänger, die in der Empfängerliste angezeigt werden sollen, benötigen die Nachricht nicht erneut. Für jeden Empfänger, die nicht zuvor die Nachricht erhalten haben, wird der Client behält den ursprünglichen Empfänger mit seinem **PR_RECIPIENT_TYPE** Wert unverändert aber darüber sendet eine Kopie des Empfängers mit MAPI_P1 anstelle der ursprüngliche Wert. Diese Kopie, die vor der Zustellung tatsächlichen gelöscht wird, erzwingt, dass den Empfänger in den Umschlag P1 und garantiert physischen erneute Übertragung an diesen Empfänger. Die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft ist für MAPI_P1 Empfänger auf FALSE festgelegt.
  
Wenn ein Client ein Formular erneut angezeigt wird, werden nur die MAPI_P1 Empfänger angezeigt. Wenn der Benutzer weitere Empfänger eingibt, wenn die Nachricht gesendet wird, wird die Empfängerliste angezeigt, genau wie beim zum ersten Mal die Nachricht gesendet wurde. 
  
Die **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) sowie die **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) Eigenschaften sind Empfängertyp relevant. Wenn ein Client eine Nachricht **IMAPIProp::SaveChanges ruft** und mindestens einen Empfänger in der Empfängerliste ist, legt der Nachricht Informationsdienst diese Eigenschaften wie folgt fest: 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_TO** Empfänger sind.  <br/> |
|PR_DISPLAY_CC  <br/> |Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_CC** Empfänger sind.  <br/> |
| PR_DISPLAY_BCC  <br/> |Auf TRUE festgelegt, wenn ein oder mehrere Empfänger **MAPI_BCC** Empfänger sind.  <br/> |
   
In x. 400 wird der Umschlag P1 oder Übermittlung benötigt, eine Nachricht, einschließlich des Empfängers Adresseigenschaften und Steuern der Übermittlung und-Antworten Optionsflags übermitteln. Der P2 oder den Anzeigenamen-Umschlag befindet sich die Informationen in der Regel auf jeden Empfänger als den Nachrichtentext selbst angezeigt. Sie umfasst in der Regel den Betreff, Wichtigkeit, Priorität, Vertraulichkeit, und Zeitpunkt der Übermittlung, sowie die primären und die kopierte Empfängernamen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagRecipientStatus (kanonische Eigenschaft)](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo (kanonische Eigenschaft)](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc (kanonische Eigenschaft)](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc (kanonische Eigenschaft)](pidtagdisplaycc-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

