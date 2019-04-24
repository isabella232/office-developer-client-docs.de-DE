---
title: Kanonische Pidtagrecipienttype (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355258"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Kanonische Pidtagrecipienttype (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Empfängertyp für einen Nachrichtenempfänger.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Kennung:  <br/> |0x0C15  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der in dieser Eigenschaft enthaltene Empfängertyp besteht aus einem erforderlichen Wert und einem optionalen Flag.
  
Diese Eigenschaft muss genau einen der folgenden Werte enthalten:
  
MAPI_TO 
  
> Der Empfänger ist ein primärer Empfänger (an). Clients müssen primäre Empfänger verarbeiten. Alle anderen Typen sind optional.
    
MAPI_CC 
  
> Der Empfänger ist ein CC-Empfänger (Carbon Copy), ein Empfänger, der zusätzlich zu den primären Empfängern eine Nachricht empfängt.
    
MAPI_BCC 
  
> Der Empfänger ist ein BCC-Empfänger (Blind Carbon Copy). Primäre und Carbon Copy-Empfänger wissen nicht, dass BCC-Empfänger vorhanden sind. 
    
MAPI_P1 
  
> Der Empfänger hat die Nachricht beim vorherigen Versuch nicht erfolgreich empfangen. Dies ist eine erneute Übermittlung einer früheren Übertragung.
    
Darüber hinaus kann das folgende Flag festgelegt werden:
  
MAPI_SUBMITTED 
  
> Der Empfänger hat die Nachricht bereits empfangen und muss ihn nicht erneut empfangen. Dies ist eine erneute Übermittlung einer früheren Übertragung. Dieses Flag wird in Verbindung mit den **MAPI_TO**-, **MAPI_CC**-und **MAPI_BCC** -Werten festgelegt. 
    
Der MAPI_P1-Wert und das **MAPI_SUBMITTED** -Flag werden verwendet, wenn eine Nachricht aufgrund einer Nichtübermittlung an einen oder mehrere der vorgesehenen Empfänger erneut übermittelt wird. Bei dieser erneuten Übertragung legt der Client **MAPI_SUBMITTED** für jeden Empfänger fest, der die Nachricht nicht erneut benötigt, sondern in der Empfängerliste angezeigt werden soll. Für jeden Empfänger, der die Nachricht zuvor nicht erhalten hat, behält der Client den ursprünglichen Empfänger mit dem **PR_RECIPIENT_TYPE** -Wert unverändert bei, gibt aber zusätzlich eine Kopie des Empfängers mit MAPI_P1 anstelle des ursprünglichen Werts aus. Diese Kopie, die vor der tatsächlichen Übermittlung verworfen wird, zwingt den Empfänger in den P1-Umschlag und garantiert eine physische erneute Übermittlung an diesen Empfänger. Die **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft ist für MAPI_P1-Empfänger auf false festgelegt.
  
Wenn ein Client ein Resend-Formular anzeigt, sind nur die MAPI_P1-Empfänger sichtbar. Wenn der Benutzer keine weiteren Empfänger eingibt, wird die Empfängerliste genau wie beim ersten Senden der Nachricht angezeigt. 
  
Die Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) **, PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_BCC** ([pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md)) beziehen sich auf den Empfängertyp. Wenn ein Client die **IMAPIProp:: SaveChanges** einer Nachricht aufruft und mindestens ein Empfänger in der Empfängerliste vorhanden ist, werden diese Eigenschaften vom Nachrichtenspeicher Anbieter wie folgt festgelegt: 
  
|**Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_TO** Empfänger ist.  <br/> |
|PR_DISPLAY_CC  <br/> |Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_CC** Empfänger ist.  <br/> |
| PR_DISPLAY_BCC  <br/> |Legen Sie den Wert auf TRUE fest, wenn mindestens einer der Empfänger **MAPI_BCC** Empfänger ist.  <br/> |
   
In X. 400 ist der P1-oder Zustellungs Umschlag die Informationen, die für die Zustellung einer Nachricht erforderlich sind, einschließlich der Adresseigenschaften des Empfängers und beliebiger Options Fahnen zur Steuerung der Zustellung und der Antworten. Der P2-oder Anzeige Umschlag stellt die Informationen dar, die in der Regel jedem anderen Empfänger als dem Nachrichtentext angezeigt werden. Sie umfasst in der Regel den Betreff, die Wichtigkeit, die Priorität, die Vertraulichkeit und die Übermittlungszeit sowie die primären und kopierten Empfängernamen. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagrecipientstatus (-Eigenschaft](pidtagrecipientstatus-canonical-property.md)
  
[Kanonische PidTagDisplayTo-Eigenschaft](pidtagdisplayto-canonical-property.md)
  
[Kanonische Pidtagdisplaybcc (-Eigenschaft](pidtagdisplaybcc-canonical-property.md)
  
[Kanonische PidTagDisplayCc-Eigenschaft](pidtagdisplaycc-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

