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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421088"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Passt die Zeiger in einem [SPropValue-Array](spropvalue.md) an, nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Anzahl der Eigenschaften im Array, auf die der  _rgprop-Parameter_ verweist. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) für die Zeiger angepasst werden sollen. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays, auf das der  _rgprop-Parameter_ verweist. 
    
 _pvBaseNeu_
  
> [in] Zeiger auf die neue Basisadresse des Arrays, auf das der  _rgprop-Parameter_ verweist. 
    
 _leiterplatte_
  
> [in, out] Optionaler Zeiger auf die Größe des durch den  _parameter pvBaseNew_ angegebenen Arrays in Bytes. Wenn nicht NULL, wird der  _Parameter "pcb"_ auf die Anzahl der Bytes festgelegt, die im  _pvD-Parameter gespeichert_ sind. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Zeiger wurden erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Ein oder beide Parameter waren ungültig, oder es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>Hinweise

Die **ScRelocProps-Funktion** arbeitet unter der Annahme, dass das Eigenschaftswertarray, für das Zeiger angepasst werden, ursprünglich in einem einzigen Aufruf zugeordnet wurde, der einem Aufruf der **ScCopyProps-Funktion** ähnelt. Wenn eine Clientanwendung oder ein Dienstanbieter mit einem Eigenschaftswert arbeitet, der aus nicht gemeinsamen Speicherblöcken erstellt wird, sollte [scCopyProps](sccopyprops.md) zum Kopieren von Eigenschaften verwendet werden. 
  
 **ScRelocProps** wird verwendet, um die Gültigkeit von Zeigern in einem [SPropValue-Array zu](spropvalue.md) erhalten. Führen Sie die folgenden Vorgänge aus, um die Gültigkeit von Zeigern beim Schreiben eines solchen Arrays auf einen Datenträger zu erhalten und es von einem Datenträger aus zu lesen: 
  
1. Rufen Sie **scRelocProps** auf dem Array auf, bevor Sie das Array und die Daten auf einen Datenträger schreiben, z. B. mit dem  _pvBaseNew-Parameter,_ der auf einen Standardwert null verweisen soll. 
    
2. Nachdem Sie das Array und die Daten von einem Datenträger gelesen haben, rufen Sie **ScRelocProps** auf dem Array auf,  _deren pvBaseOld-Parameter_ dem gleichen Standardwert entspricht, der in Schritt 1 verwendet wird. Das Array und die Daten müssen in einen Puffer gelesen werden, der mit einer einzigen Zuordnung erstellt wurde. 
    
3. Der  _Parameter "pcb"_ für **ScRelocProps** ist optional. 
    
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

