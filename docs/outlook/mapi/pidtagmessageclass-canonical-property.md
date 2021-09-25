---
title: Kanonische PidTagMessageClass-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff0ea195552fbb6bd5b0ec4c204d6b25a84f62c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619974"
---
# <a name="pidtagmessageclass-canonical-property"></a>Kanonische PidTagMessageClass-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Textzeichenfolge, die die vom Absender definierte Nachrichtenklasse identifiziert, z. B. IPM.Note. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Kennung:  <br/> |0x001A  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Nachrichtenklasse gibt den Typ der Nachricht an. Es bestimmt den Satz von Eigenschaften, die für die Nachricht definiert sind, die Art der Informationen, die die Nachricht vermittelt, und wie die Nachricht behandelt wird. 
  
Diese Eigenschaften enthalten Zeichenfolgen, die mit Punkt verkettet sind. Jede Zeichenfolge stellt eine Unterklassenebene dar. Beispiel: IPM. Beachten Sie, dass es sich um eine Unterklasse von IPM und eine Oberklasse von IPM handelt. Note.Private. 
  
Diese Eigenschaften müssen aus den ASCII-Zeichen 32 bis 127 bestehen und dürfen nicht mit einem Punkt enden (ASCII 46). Sortier- und Vergleichsvorgänge müssen sie als Zeichenfolge ohne Groß-/Kleinschreibung behandeln. Die maximal mögliche Länge beträgt 255 Zeichen. Damit MAPI-Räume Qualifizierer anfügen können, wird jedoch empfohlen, die ursprüngliche Länge unter 128 Zeichen zu halten. 
  
Jede Nachricht ist erforderlich, um diese Eigenschaften zu versehen. Normalerweise legt die Clientanwendung, die eine neue Nachricht erstellt, sie fest, sobald [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) erfolgreich zurückgegeben wird. Wenn die Eigenschaft jedoch nicht festgelegt wurde, wenn der Client [IMAPIProp::SaveChanges aufruft,](imapiprop-savechanges.md)sollte sie vom Nachrichtenspeicher auf IPM festgelegt werden. 
  
Die von mapi definierten Werte sind: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM und IPC sind nur als Oberklassen gedacht, und eine Nachricht sollte mindestens einen Unterklassenqualifizierer angefügt haben, bevor sie gespeichert oder übermittelt wird. Weitere Informationen zur Verwendung von Nachrichtenklassen finden Sie unter [Nachrichtenklassen.](mapi-message-classes.md) Listen der erforderlichen und optionalen Eigenschaften für Nachrichtenklassen finden Sie in den Unterthemen [zu Informationen zu Nachrichteneigenschaften.](message-properties-overview.md)
  
Eine benutzerdefinierte Nachrichtenklasse kann Eigenschaften in einem reservierten Bereich nur für die Verwendung mit dieser Nachrichtenklasse definieren. Weitere Informationen finden Sie unter [Informationen zu Eigenschaftsbezeichnern.](mapi-property-identifier-overview.md) 
  
Nachrichtenklassen steuern, in welchem Empfangsordner eine eingehende Nachricht gespeichert wird. Weitere Informationen finden Sie unter der [IMsgStore::GetReceiveFolderTable-Methode.](imsgstore-getreceivefoldertable.md) 
  
Weitere Informationen zur Verwendung von Nachrichtenklassen mit Formularen und Formularservern finden Sie unter [Auswählen einer Nachrichtenklasse.](choosing-a-message-class.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für die Darstellung von Voicemail- und Faxnachrichten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

