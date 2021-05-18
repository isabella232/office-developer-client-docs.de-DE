---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404470"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen einzelnen Eigenschaftswert von einem Quellspeicherort an einen Zielspeicherort. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValueDest_
  
> [out] Zeiger auf die Position, an die diese Funktion eine [SPropValue-Struktur](spropvalue.md) schreibt, die den kopierten Eigenschaftswert definiert. 
    
 _lpSPropValueSrc_
  
> [in] Zeiger auf die [SPropValue-Struktur,](spropvalue.md) die den zu kopierende Eigenschaftswert enthält. 
    
 _lpfAllocMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Arbeitsspeicher zuzuordnen, wenn der Zielspeicherort nicht groß genug ist, um die zu kopierende Eigenschaft zu speichern. 
    
 _lpvObject_
  
> [in] Zeiger auf ein Objekt, für das **MAPIAllocateMore** bei Bedarf Platz reserviert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Wert der einzelnen Eigenschaft wurde erfolgreich kopiert.
    
MAPI_E_NO_SUPPORT
  
> Es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>Hinweise

Eine Clientanwendung oder ein Dienstanbieter kann die **PropCopyMore-Funktion** verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, die frei werden soll, um sie an anderer Stelle zu verwenden. 
  
 **PropCopyMore** muss keinen Arbeitsspeicher zuweisen, es sei denn, der kopierte Eigenschaftswert weist einen Typ auf, z. B. PT_STRING8, der nicht in eine [SPropValue-Struktur passt.](spropvalue.md) Für diese großen Eigenschaften weist die Funktion Speicher mithilfe der [MAPIAllocateMore-Funktion](mapiallocatemore.md) zu, an die ein Zeiger im  _lpfAllocMore-Parameter übergeben_ wird. 
  
Injudizious Use of **PropCopyMore** fragments memory; verwenden Sie stattdessen [die ScCopyProps-Funktion.](sccopyprops.md) 
  

