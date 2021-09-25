---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6b726bbf32e6c97566471a6ae6be4c33aa7e92d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575736"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Suspends processing until one or more asynchronous operations in progress on the table have completed.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _ulTimeout_
  
> [in] Maximale Anzahl von Millisekunden, um auf den Abschluss des asynchronen Vorgangs oder der Vorgänge zu warten. Um unbegrenzt zu warten, bis der Abschluss erfolgt, legen Sie  _ulTimeout_ auf 0xFFFFFFFF fest. 
    
 _lpulTableStatus_
  
> [in, out] Bei der Eingabe entweder ein gültiger Zeiger oder NULL. Wenn  _lpulTableStatus_ bei der Ausgabe ein gültiger Zeiger ist, verweist er auf den neuesten Status der Tabelle. Wenn  _lpulTableStatus_ NULL ist, werden keine Statusinformationen zurückgegeben. Wenn **WaitForCompletion** einen nicht erfolgreichen HRESULT-Wert zurückgibt, sind die Inhalte von  _lpulTableStatus_ nicht definiert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Wartevorgang war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Das Warten auf den Abschluss asynchroner Vorgänge wird in der Tabelle nicht unterstützt.
    
MAPI_E_TIMEOUT 
  
> Der asynchrone Vorgang bzw. die asynchronen Vorgänge wurden in der angegebenen Zeit nicht abgeschlossen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::WaitForCompletion-Methode** hält die Verarbeitung an, bis asynchrone Vorgänge abgeschlossen sind, die derzeit für die Tabelle ausgeführt werden. **WaitForCompletion** kann zulassen, dass die asynchronen Vorgänge entweder vollständig abgeschlossen werden oder für eine bestimmte Anzahl von Millisekunden ausgeführt werden, wie durch  _ulTimeout_ angegeben, bevor sie unterbrochen werden. Rufen Sie die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) auf, um laufende asynchrone Vorgänge zu erkennen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

