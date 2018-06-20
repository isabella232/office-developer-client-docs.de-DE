---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795487"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Betrifft**: Outlook 
  
Passt die Zeiger in ein Array [SPropValue](spropvalue.md) , nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameter

 _cprop_
  
> [in] Anzahl der Eigenschaften im Array auf den durch den Parameter _Rgprop_ verwiesen. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die für die Zeiger sind angepasst werden. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays auf den durch den Parameter _Rgprop_ verwiesen. 
    
 _pvBaseNew_
  
> [in] Zeiger auf die neue Basisadresse des Arrays auf den durch den Parameter _Rgprop_ verwiesen. 
    
 _PCB_
  
> [in, out] Optional Zeiger auf die Größe des durch den Parameter _PvBaseNew_ angegebenen Arrays in Bytes. Wenn nicht NULL-Wert der _pcb_ -Parameter wird festgelegt, um die Anzahl von Bytes, die im Parameter _PvD_ gespeichert. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Zeiger wurden erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Einer oder beide Parameter war ungültig oder eine unbekannte Eigenschaftentyp aufgetreten.
    
## <a name="remarks"></a>Hinweise

Die Funktion **ScRelocProps** wirkt sich auf der Annahme, die das Wertearray-Eigenschaft für das Zeiger angepasst werden in einem einzigen Aufruf ähnlich einem Aufruf der Funktion **ScCopyProps** ursprünglich belegt wurde. Wenn eine Clientanwendung oder Service Provider-Eigenschaft den Wert funktionsfähig ist, die aus getrennten Blöcke des Arbeitsspeichers erstellt wird, sollte [ScCopyProps](sccopyprops.md) zum Kopieren von Eigenschaften stattdessen verwendet werden. 
  
 **ScRelocProps** wird verwendet, um die Gültigkeit der Zeiger in ein Array [SPropValue](spropvalue.md) verwalten. Um den Zeiger Gültigkeit darzustellen, wenn ein solches Array zu schreiben und Lesen Sie es von einem Datenträger, führen Sie die folgenden Vorgänge aus: 
  
1. Rufen Sie **ScRelocProps** vor dem Schreiben das Array und die Daten auf einem Datenträger, auf dem Array mit dem _PvBaseNew_ -Parameter für die Instanz auf einige Standardwert 0 (null), zeigen. 
    
2. Nach dem Lesen der Array und Daten von einem Datenträger, rufen Sie **ScRelocProps** für das Array mit dem Parameter _PvBaseOld_ , der dem in Schritt 1 verwendeten standard Wert gleich ist. Das Array und die Daten müssen in einen Puffer mit einer einzelnen Reservierung erstellt gelesen werden. 
    
3. Der Parameter _pcb_ **ScRelocProps** ist optional. 
    
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

