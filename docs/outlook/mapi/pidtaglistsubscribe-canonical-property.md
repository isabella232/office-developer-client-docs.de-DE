---
title: PidTagListSubscribe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279657"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>PidTagListSubscribe (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) List-Subscribe Kopfzeilenfeld.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Kennung:  <br/> |0x1044  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Hinweise

Um ein List-Subscribe zu generieren, müssen Clients den Wert dieser Eigenschaften auf den gewünschten Wert festlegen. MIME-Writer müssen den Wert dieser Eigenschaften in das List-Subscribe kopieren.
  
Um den Wert von serverbezogenen Eigenschaften wie diesen festlegen zu können, müssen MIME-Clients die Kopfzeilenfelder wie in der folgenden Tabelle angegeben schreiben.
  
|**Eigenschaft**|**Name des bevorzugten Kopfzeilenfelds**|**Alternativer Kopfzeilenfeldname**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |List-Subscribe  <br/> |X-List-Subscribe  <br/> |
   
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

