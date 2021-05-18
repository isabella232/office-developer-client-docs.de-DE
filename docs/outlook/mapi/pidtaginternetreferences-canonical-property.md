---
title: PidTagInternetReferences (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360410"
---
# <a name="pidtaginternetreferences-canonical-property"></a>PidTagInternetReferences (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert des Headerfelds References einer MIME-Nachricht (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Kennung:  <br/> |0x1039  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Hinweise

Um ein References-Kopfzeilenfeld zu generieren, müssen Clients diese Eigenschaften auf den gewünschten Wert festlegen. MIME-Writer müssen den Wert dieser Eigenschaften in das Kopfzeilenfeld Verweise kopieren.
  
Um den Wert dieser Eigenschaften festlegen zu können, müssen MIME-Clients den gewünschten Wert in ein References-Kopfzeilenfeld schreiben. MIME-Reader müssen den Wert des Kopfzeilenfelds Verweise in diese Eigenschaften kopieren. MIME-Reader können den Wert dieser Eigenschaften kürzen, wenn sie eine Länge von 64 KB überschreiten.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

