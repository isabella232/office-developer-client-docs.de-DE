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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563923"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ebenen eine **IStorage** -Schnittstelle auf **IStream** -Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf die **IUnknown** -Objekt **IStream**implementieren. 
    
 _lpInterface_
  
> [in] Zeiger auf der Benutzeroberfläche IID (Identifier) für das Stream-Objekt. Eines der folgenden Werte im _LpInterface_ -Parameter übergeben werden kann: NULL, IID_IStream oder IID_ILockBytes. Übergeben von NULL in _LpInterface_ ist identisch mit der Übergabe IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die steuert, wie das Objekt ist relativ zu der Stream erstellt werden soll. Die Standardeinstellung ist STGSTRM_RESET, die ermöglicht des Zugriffs nur-Lese-Speicher und startet ihn an der Position 0 (null) des Stream-Objekts. Die folgenden Kennzeichen können eine beliebige Kombination außer festgelegt werden, wie bereits erwähnt:
    
STGSTRM_CREATE 
  
> Erstellt ein neues Speicherobjekt für das Stream-Objekt. Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist. 
    
STGSTRM_CURRENT 
  
> Startet Speicher an der aktuellen Position des Datenstroms. Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist. 
    
STGSTRM_MODIFY 
  
> Ermöglicht es dem aufrufenden Dienstanbieter, in der zurückgegebene Speicher zu schreiben. Dieses Kennzeichen können nicht festgelegt werden, wenn das Flag STGSTRM_RESET festgelegt ist. 
    
STGSTRM_RESET 
  
> Startet Speicher an Position 0 (null). Dieses Kennzeichen können nicht festgelegt werden, wenn alle anderen Kennzeichen festgelegt ist. 
    
 _lppStorageOut_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene **IStorage** -Objekt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachricht speichern-Anbieter unterstützen die **HrIStorageFromStream** -Funktion mit der **IStorage** -Schnittstelle für Anlagen. Speicheranbieter müssen die **IStream** -Schnittstelle implementieren. **HrIStorageFromStream** stellt die **IStorage** -Schnittstelle für das **IStream** -Objekt. Es ist möglich, eine **ILockBytes** oder eine **IStream** -Schnittstelle in _LpUnkIn_übergeben. 
  

