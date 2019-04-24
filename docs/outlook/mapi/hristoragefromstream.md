---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347782"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Layers eine **IStorage** -Schnittstelle auf ein **IStream** -Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parameter

 _lpUnkIn_
  
> in Zeiger auf das **IUnknown** -Objekt, das **IStream**implementiert. 
    
 _lpInterface_
  
> in Zeiger auf die Schnittstellen-ID (IID) für das Stream-Objekt. Jeder der folgenden Werte kann im _lpInterface_ -Parameter übergeben werden: NULL, IID_IStream oder IID_ILockBytes. Das übergeben von NULL in _lpInterface_ ist identisch mit dem übergeben von IID_IStream. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die Steuern, wie das Speicherobjekt relativ zum Stream erstellt werden soll. Die Standardeinstellung ist STGSTRM_RESET, wodurch das Speicherobjekt schreibgeschützt ist und an Position NULL des Streams gestartet wird. Die folgenden Flags können in beliebiger Kombination festgelegt werden, außer wie angegeben:
    
STGSTRM_CREATE 
  
> Erstellt ein neues Speicherobjekt für das Stream-Objekt. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_CURRENT 
  
> Startet den Speicher an der aktuellen Position des Streams. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_MODIFY 
  
> Ermöglicht es dem aufrufenden Dienstanbieter, in den zurückgegebenen Speicher zu schreiben. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_RESET 
  
> Startet den Speicher an Position NULL. Dieses Flag kann nicht festgelegt werden, wenn ein anderes Flag festgelegt ist. 
    
 _lppStorageOut_
  
> Out Zeiger auf einen Zeiger auf das zurückgegebene **IStorage** -Objekt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Nachrichtenspeicher Anbieter unterstützen die **HrIStorageFromStream** -Funktion mithilfe der **IStorage** -Schnittstelle für Anlagen. Speicheranbieter müssen die **IStream** -Schnittstelle implementieren. **HrIStorageFromStream** stellt die **IStorage** -Schnittstelle für das **IStream** -Objekt bereit. Es ist möglich, eine **ILockBytes** oder eine **IStream** -Schnittstelle in _lpUnkIn_zu übertragen. 
  

