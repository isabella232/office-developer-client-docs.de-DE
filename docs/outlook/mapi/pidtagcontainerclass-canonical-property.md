---
title: PidTagContainerClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 423e5d5cbb2cd66f4bd47c76ef93998420072593
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571101"
---
# <a name="pidtagcontainerclass-canonical-property"></a>PidTagContainerClass (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Textzeichenfolge, die den Typ eines Ordners beschreibt. Obwohl diese Eigenschaft im Allgemeinen ignoriert wird, erwarten Versionen von Microsoft® Exchange Server vor Exchange Server 2003 Mailbox Manager, dass diese Eigenschaft vorhanden ist.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Kennung:  <br/> |0x3613  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaften werden normalerweise nicht von Exchange Server verwendet. Microsoft Office Outlook® fügt sie jedoch Postfachordnern zu. Darüber hinaus behandeln Versionen von Exchange Server vor Exchange Server 2003 Mailbox Manager möglicherweise falsch Ordner, die nicht über diese Eigenschaften verfügen.
  
Diesen Eigenschaften können die Zeichenfolgenwerte in der folgenden Tabelle zugewiesen werden.
  
|**Wert**|**Inhalt des Ordners**|
|:-----|:-----|
|IPF.Appointment  <br/> |Termine  <br/> |
|IPF.Contact  <br/> |Kontakte  <br/> |
|IPF. Journal  <br/> |Outlook Journaleinträge  <br/> |
|IPF.Note  <br/> |E-Mail-Nachrichten und Notizen  <br/> |
|IPF. Stickynote  <br/> |Outlook Kurznotizen  <br/> |
|IPF.Task  <br/> |Outlook-Aufgaben  <br/> |
   
Für Ordner, die E-Mail-Nachrichten enthalten, sollten diese Eigenschaften auf IPF festgelegt werden. Hinweis.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlistenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

