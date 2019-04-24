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
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360690"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Passt die Zeiger in einem [SPropValue](spropvalue.md) -Array an, nachdem das Array und seine Daten kopiert oder an einen neuen Speicherort verschoben wurden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Die Anzahl der Eigenschaften im Array, auf die durch den _rgprop_ -Parameter verwiesen wird. 
    
 _rgprop_
  
> in Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, für die Zeiger angepasst werden sollen. 
    
 _pvBaseOld_
  
> in Zeiger auf die ursprüngliche Basisadresse des Arrays, auf das durch den _rgprop_ -Parameter verwiesen wird. 
    
 _pvBaseNew_
  
> in Zeiger auf die neue Basisadresse des Arrays, auf das durch den _rgprop_ -Parameter verwiesen wird. 
    
 _PCB_
  
> [in, out] Optionaler Zeiger auf die Größe des vom _pvBaseNew_ -Parameter angegebenen Arrays in Byte. Wenn dies nicht der Fall ist, wird der _PCB_ -Parameter auf die im _PVD_ -Parameter gespeicherte Anzahl von Bytes festgelegt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Zeiger wurden erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Ein oder beide Parameter waren ungültig, oder es wurde ein unbekannter Eigenschaftentyp gefunden.
    
## <a name="remarks"></a>Bemerkungen

Die **ScRelocProps** -Funktion wird davon ausgegangen, dass das Eigenschafts Wertarray, für das Zeiger angepasst wurden, ursprünglich in einem einzelnen Aufruf zugeordnet wurde, der einem Aufruf der **ScCopyProps** -Funktion ähnelt. Wenn eine Clientanwendung oder ein Dienstanbieter mit einem Eigenschaftswert arbeitet, der aus nicht zusammengestellten Speicherblöcken erstellt wurde, sollte er [ScCopyProps](sccopyprops.md) verwenden, um stattdessen Eigenschaften zu kopieren. 
  
 **ScRelocProps** wird verwendet, um die Gültigkeit von Zeigern in einem [SPropValue](spropvalue.md) -Array zu behalten. Führen Sie die folgenden Schritte aus, um die Gültigkeit von Zeiger beim Schreiben eines solchen Arrays in und von einem Datenträger zu erhalten: 
  
1. Bevor Sie das Array und die Daten auf einen Datenträger schreiben, rufen Sie **ScRelocProps** auf dem Array mit dem _pvBaseNew_ -Parameter auf, der auf einen Standardwert 0 (null) zeigt. 
    
2. Nachdem Sie das Array und die Daten von einem Datenträger gelesen haben, rufen Sie **ScRelocProps** im Array mit dem Parameter _pvBaseOld_ auf, der dem gleichen Standardwert entspricht, der in Schritt 1 verwendet wird. Das Array und die Daten müssen in einen mit einer einzelnen Zuordnung erstellten Puffer eingelesen werden. 
    
3. Der _PCB_ -Parameter für **ScRelocProps** ist optional. 
    
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

