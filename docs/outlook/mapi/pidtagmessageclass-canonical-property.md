---
title: PidTagMessageClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f54bdb70e9f48c89cb50e8238f8638deac8a93b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567818"
---
# <a name="pidtagmessageclass-canonical-property"></a>PidTagMessageClass (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Textzeichenfolge, die die Absender benutzerdefinierte Nachrichtenklasse wie IPM identifiziert. Beachten Sie. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Kennung:  <br/> |0x001A  <br/> |
|Datentyp:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Bereich:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Nachrichtenklasse gibt den Typ der Nachricht. Bestimmt den Satz von Eigenschaften, die für die Nachricht definiert die Art von Informationen die Nachricht übermittelt, und wie die Meldung zu behandeln. 
  
Diese Eigenschaften enthalten mit Perioden verkettete Zeichenfolgen. Jede Zeichenfolge stellt eine Ebene von Unterklassen dar. Beispielsweise IPM. Hinweis: ist eine Unterklasse der IPM und eine übergeordnete Klasse von IPM. Note.Private. 
  
Diese Eigenschaften müssen den ASCII-Zeichen 32 bis 127 bestehen und darf nicht mit einem Punkt (ASCII-46) enden. Sortieren und vergleichen Vorgänge müssen sie als ein Zeichenfolgenvergleich behandeln. Die maximale mögliche Länge beträgt 255 Zeichen, aber, um MAPI Platz Qualifizierer anzufügende bereitsteht wird empfohlen, dass die ursprüngliche Länge unter 128 Zeichen behandelt werden. 
  
Jede Nachricht ist erforderlich, um diese Eigenschaften bereitzustellen. Normalerweise wird die Client-Anwendung eine neue Nachricht erstellen, sobald [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) erfolgreich zurückgegeben wird. Aber wenn die Eigenschaft, wenn der Client [IMAPIProp::SaveChanges](imapiprop-savechanges.md)ruft nicht festgelegt wurde, der Nachrichtenspeicher sollte auf festlegen IPM. 
  
Die Werte von MAPI definiert sind: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM und IPK dienen nur Klassen werden, und eine Nachricht sollte mindestens eine Unterklasse Qualifizierer angefügt, bevor Sie gespeichert oder gesendet wird. Weitere Informationen über die Verwendung der Nachricht-Klasse finden Sie unter [Message Classes](mapi-message-classes.md). Liste der erforderlichen und optionalen Eigenschaften für Nachrichtenklassen finden Sie unter der untergeordneten Themen mit [Informationen zu Nachrichteneigenschaften](message-properties-overview.md).
  
Eine benutzerdefinierte Nachrichtenklasse kann Eigenschaften in einem reservierten Bereich für die Verwendung mit nur die Nachrichtenklasse definieren. Weitere Informationen finden Sie unter [Informationen zu Eigenschaftskennungen](mapi-property-identifier-overview.md). 
  
Nachricht Klassen steuern, welche die Ordner eine eingehende Nachricht empfangen wird in gespeichert. Weitere Informationen finden Sie unter der [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode. 
  
Weitere Informationen zur Verwendung von Nachrichtenklassen mit Formularen und Form-Servern finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für das Darstellen von Voicemail- und Sprachnachrichten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

