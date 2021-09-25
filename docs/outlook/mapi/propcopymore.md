---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ba233885e8173a978f3884943ebc358e39b78d2c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578858"
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
  
> [in] Zeiger auf die [SPropValue-Struktur,](spropvalue.md) die den zu kopierenden Eigenschaftswert enthält. 
    
 _lpfAllocMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen, wenn der Zielspeicherort nicht groß genug ist, um die zu kopierende Eigenschaft zu speichern. 
    
 _lpvObject_
  
> [in] Zeiger auf ein Objekt, für das **MAPIAllocateMore** bei Bedarf Speicherplatz zuweist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der einzelne Eigenschaftswert wurde erfolgreich kopiert.
    
MAPI_E_NO_SUPPORT
  
> Es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung oder ein Dienstanbieter kann die **PropCopyMore-Funktion** verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, die freigegeben werden soll, um sie an anderer Stelle zu verwenden. 
  
 **PropCopyMore** muss keinen Speicher zuordnen, es sei denn, der kopierte Eigenschaftswert hat einen Typ, z. B. PT_STRING8, der nicht in eine [SPropValue-Struktur](spropvalue.md) passt. Für diese großen Eigenschaften weist die Funktion Speicher mithilfe der [MAPIAllocateMore-Funktion](mapiallocatemore.md) zu, an die ein Zeiger im  _Parameter lpfAllocMore_ übergeben wird. 
  
Judizierte Verwendung des **PropCopyMore-Fragmentspeichers;** Erwägen Sie stattdessen die Verwendung der [ScCopyProps-Funktion.](sccopyprops.md) 
  

