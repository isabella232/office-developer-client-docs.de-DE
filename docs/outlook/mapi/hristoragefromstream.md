---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fed8b12b1541e0ca952fc54ff9028c49d11d600f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610776"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt eine **IStorage-Schnittstelle** auf ein **IStream-Objekt** fest. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf das **IUnknown** -Objekt, das **IStream** implementiert. 
    
 _lpInterface_
  
> [in] Zeiger auf den Schnittstellenbezeichner (IID) für das Streamobjekt. Jeder der folgenden Werte kann im  _lpInterface-Parameter_ übergeben werden: NULL, IID_IStream oder IID_ILockBytes. Das Übergeben von NULL in  _lpInterface_ entspricht der Übergabe IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie das Speicherobjekt relativ zum Datenstrom erstellt werden soll. Die Standardeinstellung ist STGSTRM_RESET. Dadurch erhält das Speicherobjekt schreibgeschützten Zugriff und startet es an Position 0 des Datenstroms. Die folgenden Flags können in einer beliebigen Kombination festgelegt werden, außer wie bereits erwähnt:
    
STGSTRM_CREATE 
  
> Erstellt ein neues Speicherobjekt für das Datenstromobjekt. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_CURRENT 
  
> Startet den Speicher an der aktuellen Position des Datenstroms. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_MODIFY 
  
> Ermöglicht dem aufrufenden Dienstanbieter, in den zurückgegebenen Speicher zu schreiben. Dieses Flag kann nicht festgelegt werden, wenn das STGSTRM_RESET-Flag festgelegt ist. 
    
STGSTRM_RESET 
  
> Startet den Speicher an Position 0. Dieses Kennzeichen kann nicht festgelegt werden, wenn ein anderes Flag festgelegt ist. 
    
 _lppStorageOut_
  
> [out] Zeiger auf einen Zeiger auf das **zurückgegebene IStorage-Objekt.** 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachrichtenspeicheranbieter unterstützen die **HrIStorageFromStream-Funktion** mithilfe der **IStorage-Schnittstelle** für Anlagen. Store Anbieter müssen die **IStream-Schnittstelle** implementieren. **HrIStorageFromStream** stellt die **IStorage-Schnittstelle** für das **IStream-Objekt** bereit. Es ist möglich, eine **ILockBytes-** oder **eine IStream-Schnittstelle** in  _lpUnkIn_ zu übergeben. 
  

