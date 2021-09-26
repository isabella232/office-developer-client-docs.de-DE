---
title: Kanonische PidTagControlType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 059fc990a3d5644878e2fc7990e49565b3f9da53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583520"
---
# <a name="pidtagcontroltype-canonical-property"></a>Kanonische PidTagControlType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der einen Steuerelementtyp für ein Steuerelement angibt, das in einem Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_TYPE  <br/> |
|Kennung:  <br/> |0x3F02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann genau einen der folgenden Werte haben:
    
DTCT_LABEL (0x00000000)
  
> Eine Dialogbeschriftung.
   
DTCT_EDIT (0x00000001)
  
> Ein Dialogfeld zum Bearbeiten von Text.

DTCT_LBX (0x00000002)
  
> Ein Dialogfeld.
    
DTCT_COMBOBOX (0x00000003)
  
> Ein Dialogfeld-Kombinationsfeld.

DTCT_DDLBX (0x00000004)
  
> Ein Dialogfeld-Dropdown-Listenfeld.

DTCT_CHECKBOX (0x00000005)
  
> Ein Dialogfeld.

DTCT_GROUPBOX (0x00000006)
  
> Ein Dialogfeld für eine Gruppe.
  
DTCT_BUTTON (0x00000007)
  
> Ein Dialogfeld-Steuerelement.
    
DTCT_PAGE (0x00000008)
  
> Eine Dialogseite mit Registerkarten.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Ein Dialogfeld-Optionsfeld.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Ein mehrwertiges Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ "String" aufgefüllt wird.
    
DTCT_MVDDLBX (0x0000000C)
  
> Ein mehrwertiges Dropdown-Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ String ausgefüllt wird.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

