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
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355258"
---
# <a name="pidtagrecipienttype-canonical-property"></a>PidTagRecipientType (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Empfängertyp für einen Nachrichtenempfänger.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Kennung:  <br/> |0x0C15  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Der in dieser Eigenschaft enthaltene Empfängertyp besteht aus einem erforderlichen Wert und einem optionalen Flag.
  
Diese Eigenschaft muss genau einen der folgenden Werte enthalten:
  
MAPI_TO 
  
> Der Empfänger ist ein primärer (An)-Empfänger. Clients sind für die Verarbeitung primärer Empfänger erforderlich. Alle anderen Typen sind optional.
    
MAPI_CC 
  
> Der Empfänger ist ein Cc-Empfänger (Carbon Copy), ein Empfänger, der zusätzlich zu den primären Empfängern eine Nachricht empfängt.
    
MAPI_BCC 
  
> Der Empfänger ist ein Blind Carbon Copy (BCC)-Empfänger. Primäre Empfänger und Empfänger von Carbonkopien sind sich des Vorhandenseins von BCC-Empfängern nicht bewusst. 
    
MAPI_P1 
  
> Der Empfänger hat die Nachricht beim vorherigen Versuch nicht erfolgreich empfangen. Dies ist ein erneutes Senden einer früheren Übertragung.
    
Darüber hinaus kann das folgende Flag festgelegt werden:
  
MAPI_SUBMITTED 
  
> Der Empfänger hat die Nachricht bereits empfangen und muss sie nicht erneut empfangen. Dies ist ein erneutes Senden einer früheren Übertragung. Dieses Flag wird in Verbindung mit den Werten **MAPI_TO**, **MAPI_CC** und **MAPI_BCC** festgelegt. 
    
Der MAPI_P1-Wert und das **MAPI_SUBMITTED** werden verwendet, wenn eine Nachricht aufgrund einer Nichtübereinstellung an einen oder mehrere der beabsichtigten Empfänger erneut gesendet wird. Für diese erneute Übertragung legt  der Client MAPI_SUBMITTED empfänger fest, der die Nachricht nicht erneut benötigt, aber in der Empfängerliste angezeigt werden soll. Für jeden Empfänger, der die Nachricht zuvor nicht empfangen hat, behält der Client den ursprünglichen Empfänger mit seinem **PR_RECIPIENT_TYPE-Wert** unverändert bei, sendet aber zusätzlich eine Kopie des Empfängers mit MAPI_P1 an Stelle des ursprünglichen Werts. Diese Kopie, die vor der tatsächlichen Zustellung verworfen wird, zwingt den Empfänger in den Briefumschlag P1 und garantiert die physische Weiterübertragung an diesen Empfänger. Die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) -Eigenschaft ist auf FALSE für MAPI_P1 festgelegt.
  
Wenn ein Client ein erneut gesendetes Formular anzeigt, sind nur MAPI_P1 Empfänger sichtbar. Wenn der Benutzer keine weiteren Empfänger einbetritt, wird die Empfängerliste bei zugestellter Nachricht genau wie beim ersten Senden der Nachricht angezeigt. 
  
Die **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) sind mit dem Empfängertyp verknüpft. Wenn ein Client die **IMAPIProp::SaveChanges** einer Nachricht aufruft und mindestens ein Empfänger in der Empfängerliste vorhanden ist, legt der Nachrichtenspeicheranbieter die folgenden Eigenschaften fest: 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Wird auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_TO** ist.  <br/> |
|PR_DISPLAY_CC  <br/> |Wird auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_CC** ist.  <br/> |
| PR_DISPLAY_BCC  <br/> |Wird auf TRUE festgelegt, wenn mindestens einer der Empfänger **MAPI_BCC** ist.  <br/> |
   
In X.400 ist der Briefumschlag P1 oder der Zustellumschlag die Informationen, die zum Senden einer Nachricht benötigt werden, einschließlich der Adresseigenschaften des Empfängers und aller Optionskennzeichen, die die Zustellung und Antworten steuern. Bei dem P2- oder Displayumschlag handelt es sich um die Informationen, die in der Regel jedem empfänger anderen Empfänger als dem Nachrichtentext selbst angezeigt werden. Sie umfasst in der Regel den Betreff, die Wichtigkeit, die Priorität, die Vertraulichkeit und die Übermittlungszeit sowie die primären und kopierten Empfängernamen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagRecipientStatus (kanonische Eigenschaft)](pidtagrecipientstatus-canonical-property.md)
  
[PidTagDisplayTo (kanonische Eigenschaft)](pidtagdisplayto-canonical-property.md)
  
[PidTagDisplayBcc (kanonische Eigenschaft)](pidtagdisplaybcc-canonical-property.md)
  
[PidTagDisplayCc (kanonische Eigenschaft)](pidtagdisplaycc-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

