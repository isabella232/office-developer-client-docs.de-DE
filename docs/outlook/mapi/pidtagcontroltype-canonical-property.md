---
title: Kanonische pidtagcontroltype (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734203"
---
# <a name="pidtagcontroltype-canonical-property"></a>Kanonische pidtagcontroltype (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der einen Steuerelementtyp für ein in einem Dialogfeld verwendetes Steuerelement angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_TYPE  <br/> |
|Kennung:  <br/> |0x3F02  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
    
DTCT_LABEL (0x00000000)
  
> Eine Dialogfeld Bezeichnung.
   
DTCT_EDIT (0x00000001)
  
> Ein Dialogfeld Bearbeitungstextfeld.

DTCT_LBX (0x00000002)
  
> Dialog-Listenfeld.
    
DTCT_COMBOBOX (0x00000003)
  
> Ein Dialogfeld-Kombinationsfeld.

DTCT_DDLBX (0x00000004)
  
> Ein Dropdown-Listenfeld für Dialogfelder.

DTCT_CHECKBOX (0x00000005)
  
> Ein Kontrollkästchen für ein Dialogfeld.

DTCT_GROUPBOX (0x00000006)
  
> Dialoggruppen Feld.
  
DTCT_BUTTON (0x00000007)
  
> Ein Dialogfeld-Steuerelement.
    
DTCT_PAGE (0x00000008)
  
> Seite mit Registerkarten im Dialogfeld.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Optionsfeld "Dialog".
    
DTCT_MVLISTBOX (0x0000000B)
  
> Ein mehrwertiges Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ String aufgefüllt wird.
    
DTCT_MVDDLBX (0x0000000C)
  
> Ein mehrwertiges Dropdown-Listenfeld, das von einer mehrwertigen Eigenschaft vom Typ String aufgefüllt wird.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet werden.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

