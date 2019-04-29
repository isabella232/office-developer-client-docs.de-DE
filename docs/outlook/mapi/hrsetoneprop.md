---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417658"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den Wert einer einzelnen Eigenschaft für eine Eigenschaften Schnittstelle fest oder ändert Sie, also eine von [IMAPIProp](imapipropiunknown.md)abgeleitete Schnittstelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameter

 _PMP_
  
> in Zeiger auf eine [IMAPIProp](imapipropiunknown.md) -Schnittstelle, auf der der Eigenschaftswert festgelegt oder geändert werden soll. 
    
 _pprop_
  
> in Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die den Wert definiert, der für die _PMP_ -Eigenschaft festgelegt werden soll. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Im Gegensatz zur [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode gibt die **HrSetOneProp** -Funktion nie Warnungen zurück. Da nur eine Eigenschaft festgelegt wird, wird Sie entweder erfolgreich ausgeführt oder schlägt fehl. Zum Festlegen oder ändern mehrerer Eigenschaften ist **** SetProps schneller. 
  
Sie können eine einzelne Eigenschaft mit der [HrGetOneProp](hrgetoneprop.md) -Funktion abrufen. 
  

