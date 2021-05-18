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
  
Die Verarbeitung wird angehalten, bis ein oder mehrere asynchrone Vorgänge in der Tabelle abgeschlossen sind.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss null sein.
    
 _ulTimeout_
  
> [in] Maximale Anzahl von Millisekunden, bis der asynchrone Vorgang abgeschlossen ist. Legen Sie  _ulTimeout_ auf 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] Bei der Eingabe entweder ein gültiger Zeiger oder NULL. Wenn  _lpulTableStatus_ bei der Ausgabe ein gültiger Zeiger ist, zeigt er auf den neuesten Status der Tabelle. Wenn  _lpulTableStatus_ NULL ist, werden keine Statusinformationen zurückgegeben. Wenn **WaitForCompletion** einen nicht erfolgreichen HRESULT-Wert zurückgibt, ist der Inhalt von  _lpulTableStatus_ nicht definiert. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Wartevorgang war erfolgreich.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt nicht das Warten auf den Abschluss asynchroner Vorgänge.
    
MAPI_E_TIMEOUT 
  
> Der asynchrone Vorgang oder die asynchronen Vorgänge wurden zum angegebenen Zeitpunkt nicht abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::WaitForCompletion-Methode** setzt die Verarbeitung aus, bis alle derzeit für die Tabelle ausgeführten asynchronen Vorgänge abgeschlossen sind. **WaitForCompletion** kann zulassen, dass die asynchronen Vorgänge entweder vollständig abgeschlossen oder für eine bestimmte Anzahl von Millisekunden ausgeführt werden, wie von  _ulTimeout_ angegeben, bevor sie unterbrochen werden. Rufen Sie die [IMAPITable::GetStatus-Methode](imapitable-getstatus.md) auf, um asynchrone Vorgänge zu erkennen, die ausgeführt werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

