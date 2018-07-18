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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795316"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Betrifft**: Outlook 
  
Kopiert einen einzelnen Eigenschaftswert von einem Quellspeicherort in einen Zielspeicherort. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [out] Zeiger auf den Speicherort, zu dem diese Funktion eine [SPropValue](spropvalue.md) -Struktur definieren den kopierten Eigenschaftswert schreibt. 
    
 _lpSPropValueSrc_
  
> [in] Zeiger auf die [SPropValue](spropvalue.md) -Struktur, die Wert der Eigenschaft kopiert werden soll. 
    
 _lpfAllocMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die verwendet werden, um zusätzliche Speicher ist Zielspeicherort nicht groß genug für die Eigenschaft kopiert werden soll. 
    
 _lpvObject_
  
> [in] Zeiger auf ein Objekt für die **MAPIAllocateMore** Speicherplatz bei Bedarf reserviert werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Die einzelnen Eigenschaftswert wurde erfolgreich kopiert.
    
MAPI_E_NO_SUPPORT
  
> Unbekannte Eigenschaft vom Typ aufgetreten.
    
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder Dienstanbieter kann die Funktion **PropCopyMore** verwenden, um eine Eigenschaft aus einer Tabelle zu kopieren, der freigegeben werden, damit er an anderer Stelle verwendet. 
  
 **PropCopyMore** muss kein Speicher zugewiesen werden, wenn der Wert der Eigenschaft kopiert eines Typs, beispielsweise PT_STRING8, ist, die nicht in einer Struktur [SPropValue](spropvalue.md) passen. Für diese Eigenschaften großen weist die Funktion Speicher, die mithilfe der [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die ein Zeiger in der _LpfAllocMore_ -Parameter übergeben wird. 
  
Injudicious Verwendung von **PropCopyMore** Fragmente Speicher; Erwägen Sie die [ScCopyProps](sccopyprops.md) -Funktion. 
  

