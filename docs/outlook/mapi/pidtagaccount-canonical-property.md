---
title: Kanonische PidTagAccount-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359780"
---
# <a name="pidtagaccount-canonical-property"></a>Kanonische PidTagAccount-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Kontonamen des Empfängers. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Kennung:  <br/> |0x3A00  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften bieten Identifizierungs-und Zugriffsinformationen für einen Empfänger. Sie werden vom Empfänger und dessen Organisation definiert.
  
Diese Eigenschaften enthalten in der Regel den e-Mail-Namen des Empfängers, also die letzte Komponente der e-Mail-Adresse, die den Empfänger in der lokalen Organisation eindeutig identifiziert. Der Name der e-Mail-Adresse entspricht dem Distinguished Name X. 400, der ein kurzer Name sein soll, der in einer bestimmten Messaging Domäne garantiert eindeutig ist.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Header Dateien

mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

