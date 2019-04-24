---
title: Kanonische PidTagMessageClass-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359263"
---
# <a name="pidtagmessageclass-canonical-property"></a>Kanonische PidTagMessageClass-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Textzeichenfolge, die die Absender definierte Nachrichtenklasse identifiziert, beispielsweise IPM. Hinweis. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Kennung:  <br/> |0x001A  <br/> |
|Datentyp:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Bereich:  <br/> |Standard  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Message-Klasse gibt den Typ der Nachricht an. Sie bestimmt die für die Nachricht definierten Eigenschaften, die Art der Informationen, über die die Nachricht vermittelt wird, und die Behandlung der Nachricht. 
  
Diese Eigenschaften enthalten Zeichenfolgen, die mit Punkten verkettet sind. Jede Zeichenfolge stellt eine Ebene der Unterklasse dar. Beispiel: IPM. Hinweis ist eine Unterklasse von IPM und eine Oberklasse von IPM. Note. private. 
  
Diese Eigenschaften müssen aus den ASCII-Zeichen 32 bis 127 bestehen und dürfen nicht mit einem Punkt (ASCII 46) enden. Sort-und Compare-Vorgänge müssen Sie als Zeichenfolge mit Groß-/Kleinschreibung behandeln. Die maximal zulässige Länge beträgt 255 Zeichen, aber um MAPI-Speicherplatz für die Anfügung von Qualifizierern zu ermöglichen, empfiehlt es sich, die ursprüngliche Länge unter 128 Zeichen zu halten. 
  
Jede Nachricht ist erforderlich, um diese Eigenschaften bereitzustellen. NormalerWeise legt die Clientanwendung, die eine neue Nachricht erstellt, Sie fest, sobald [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) erfolgreich zurückgegeben wird. Wenn die Eigenschaft jedoch nicht festgelegt wurde, wenn der Client [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)aufruft, sollte der Nachrichtenspeicher diesen auf IPM festlegen. 
  
Die von MAPI definierten Werte sind: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM und IPC sollen nur übergeordnete Klassen sein, und eine Nachricht sollte mindestens einen Unterklassen Qualifizierer angefügt haben, bevor Sie gespeichert oder übermittelt wird. Weitere Informationen zur Verwendung von Nachrichtenklassen finden Sie unter [Nachrichtenklassen](mapi-message-classes.md). Eine Liste der erforderlichen und optionalen Eigenschaften für Nachrichtenklassen finden Sie in den Unterthemen [zu Nachrichteneigenschaften](message-properties-overview.md).
  
Eine benutzerdefinierte Nachrichtenklasse kann Eigenschaften in einem reservierten Range definieren, die nur für diese Nachrichtenklasse verwendet werden können. Weitere Informationen finden Sie unter [about Property Identifiers](mapi-property-identifier-overview.md). 
  
Nachrichtenklassen steuern, in welchem Empfangsordner eine eingehende Nachricht gespeichert wird. Weitere Informationen finden Sie unter der [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode. 
  
Weitere Informationen zur Verwendung von Nachrichtenklassen mit Formularen und Formular Servern finden Sie unter [Choosing a Message Class](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für die Darstellung von Voicemail und Faxnachrichten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

