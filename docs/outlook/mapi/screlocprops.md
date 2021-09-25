---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 096ce1fbf8778c23eaf31b8008793070ffedd1af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578704"
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
  
> [in] Anzahl der Eigenschaften im Array, auf die durch den  _rgprop-Parameter_ verwiesen wird. 
    
 _rgprop_
  
> [in] Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) für die Zeiger angepasst werden sollen. 
    
 _pvBaseOld_
  
> [in] Zeiger auf die ursprüngliche Basisadresse des Arrays, auf das durch den  _rgprop-Parameter_ verwiesen wird. 
    
 _pvBaseNew_
  
> [in] Zeiger auf die neue Basisadresse des Arrays, auf das der  _rgprop-Parameter_ verweist. 
    
 _Pcb_
  
> [in, out] Optionaler Zeiger auf die Größe des Arrays in Byte, die durch den  _parameter pvBaseNew_ angegeben wird. Wenn nicht NULL, wird der  _Parameter "parameters"_ auf die Anzahl von Bytes festgelegt, die im  _PVD-Parameter_ gespeichert sind. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Zeiger wurden erfolgreich angepasst.
    
MAPI_E_INVALID_PARAMETER
  
> Ein oder beide Parameter waren ungültig, oder es wurde ein unbekannter Eigenschaftstyp gefunden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ScRelocProps-Funktion** geht davon aus, dass das Eigenschaftswertarray, für das Zeiger angepasst werden, ursprünglich in einem einzigen Aufruf zugewiesen wurde, ähnlich einem Aufruf der **ScCopyProps-Funktion.** Wenn eine Clientanwendung oder ein Dienstanbieter mit einem Eigenschaftswert arbeitet, der aus nicht zusammenhängenden Speicherblöcken erstellt wird, sollte [scCopyProps](sccopyprops.md) stattdessen zum Kopieren von Eigenschaften verwendet werden. 
  
 **ScRelocProps** wird verwendet, um die Gültigkeit von Zeigern in einem [SPropValue-Array](spropvalue.md) aufrechtzuerhalten. Führen Sie die folgenden Vorgänge aus, um die Gültigkeit von Zeigern beizubehalten, wenn Sie ein solches Array schreiben und von einem Datenträger lesen: 
  
1. Rufen Sie vor dem Schreiben des Arrays und der Daten auf einen Datenträger **ScRelocProps** für das Array auf, wobei der  _Parameter "pvBaseNew"_ beispielsweise auf einen Standardwert null verweist. 
    
2. Rufen Sie nach dem Lesen des Arrays und der Daten von einem Datenträger **ScRelocProps** für das Array mit dem  _Parameter "pvBaseOld"_ auf, der dem in Schritt 1 verwendeten Standardwert entspricht. Das Array und die Daten müssen in einen Puffer gelesen werden, der mit einer einzelnen Zuordnung erstellt wurde. 
    
3. Der  _Parameter "parameter"_ für **"ScRelocProps"** ist optional. 
    
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

