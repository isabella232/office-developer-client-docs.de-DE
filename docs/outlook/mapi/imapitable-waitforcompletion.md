---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407060"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Hält die Verarbeitung an, bis mindestens ein asynchroner Vorgang abgeschlossen ist, der in der Tabelle ausgeführt wurde.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert muss NULL sein.
    
 _ulTimeout_
  
> in Maximale Anzahl von Millisekunden, die gewartet werden soll, bis der asynchrone Vorgang abgeschlossen ist. Wenn auf unbestimmte Zeit gewartet werden soll, bis der Abschluss auftritt, legen Sie _ulTimeout_ auf 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger oder NULL. Wenn _lpulTableStatus_ ein gültiger Zeiger ist, zeigt er auf den letzten Status der Tabelle. Wenn _lpulTableStatus_ ist, werden keine Statusinformationen zurückgegeben. Wenn **WaitForCompletion** einen nicht erfolgreichen HRESULT-Wert zurückgibt, sind die Inhalte von _lpulTableStatus_ nicht definiert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Wartevorgang war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt nicht das warten auf den Abschluss von asynchronen Vorgängen.
    
MAPI_E_TIMEOUT 
  
> Der asynchrone Vorgang oder die Vorgänge wurden nicht in der angegebenen Zeit abgeschlossen.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPITable:: WaitForCompletion** -Methode wird die Verarbeitung angehalten, bis alle asynchronen Vorgänge, die für die Tabelle ausgeführt werden, abgeschlossen sind. **WaitForCompletion** kann die asynchrone Vorgänge vollständig abgeschlossen oder für eine bestimmte Anzahl von Millisekunden ausgeführt, wie durch _ulTimeout_, bevor Sie unterbrochen wird. Um asynchrone Vorgänge zu finden, die ausgeführt werden, rufen Sie die [IMAPITable:: GetStatus](imapitable-getstatus.md) -Methode auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

