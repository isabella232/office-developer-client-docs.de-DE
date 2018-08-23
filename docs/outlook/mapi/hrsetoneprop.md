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
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569127"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt fest oder ändert den Wert einer einzelnen Eigenschaft für eine Eigenschaft Schnittstelle, d. h., eine Schnittstelle [IMAPIProp](imapipropiunknown.md)abgeleitet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameter

 _PMP_
  
> [in] Zeiger auf eine [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die auf der Wert der Eigenschaft ist festgelegt oder geändert werden. 
    
 _pprop_
  
> [in] Zeiger auf die [SPropValue](spropvalue.md) -Struktur definiert, des Werts der _Pmp_ -Eigenschaft festgelegt werden soll. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zu der [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode gibt die **HrSetOneProp** Funktion nie alle Warnungen. Da nur eine Eigenschaft festgelegt, es einfach entweder Erfolg oder Fehler. Für die Einstellung oder mehrere Eigenschaften ändern ist **SetProps** schneller. 
  
Sie können eine einzelne Eigenschaft mit der Funktion [HrGetOneProp](hrgetoneprop.md) abrufen. 
  

