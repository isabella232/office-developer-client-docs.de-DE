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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792477"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Betrifft**: Outlook 
  
Unterbricht die Verarbeitung, bis eine oder mehrere asynchrone Vorgänge in Bearbeitung in der Tabelle abgeschlossen haben.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert. NULL muss sein.
    
 _ulTimeout_
  
> [in] Maximale Anzahl von Millisekunden zu warten, bis der asynchrone Vorgang oder Vorgänge abgeschlossen. Legen Sie zum Warten auf unbestimmte Zeit, bis Abschluss auftritt, _UlTimeout_ auf 0xFFFFFFFF ein. 
    
 _lpulTableStatus_
  
> [in, out] Bei der Eingabe ein gültiger Zeiger oder NULL. Bei der Ausgabe ist _LpulTableStatus_ gültiger Zeiger ist, zeigt es auf den aktuellen Status der Tabelle. Wenn _LpulTableStatus_ NULL ist, werden keine Statusinformationen zurückgegeben. Wenn **WaitForCompletion** nicht erfolgreichen HRESULT-Wert zurückgibt, sind der Inhalt der _LpulTableStatus_ nicht definiert. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Wait-Vorgang wurde erfolgreich abgeschlossen.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle unterstützt keine Anzeige für wartende für den Abschluss der asynchronen Vorgänge.
    
MAPI_E_TIMEOUT 
  
> Die asynchrone Operation oder Vorgänge wurde nicht in der angegebenen Zeit abgeschlossen.
    
## <a name="remarks"></a>Hinweise

Die Methode **IMAPITable::WaitForCompletion** hält die Verarbeitung, bis alle derzeit asynchrone Vorgänge für die Tabelle abgeschlossen haben. **WaitForCompletion** können die asynchrone Vorgänge entweder vollständig abgeschlossen oder für eine bestimmte Anzahl von Millisekunden auszuführen, wie _UlTimeout_, abgebrochen wird angegeben. Zum Erkennen von asynchrone Vorgänge in Bearbeitung rufen Sie die [IMAPITable::GetStatus](imapitable-getstatus.md) -Methode auf. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[Methode IMAPITable:: Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[SortTable](imapitable-sorttable.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

