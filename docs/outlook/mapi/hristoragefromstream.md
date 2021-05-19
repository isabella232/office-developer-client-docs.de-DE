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
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416832"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
**Überschichtt eine IStorage-Schnittstelle** auf ein **IStream-Objekt.** 
  
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
  
> [in] Zeiger auf das **IUnknown-Objekt,** das **IStream implementieren soll.** 
    
 _lpInterface_
  
> [in] Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) für das Stream-Objekt. Jeder der folgenden Werte kann im  _lpInterface-Parameter_ übergeben werden: NULL, IID_IStream oder IID_ILockBytes. Das Übergeben von NULL in  _lpInterface_ ist identisch mit dem Übergeben IID_IStream. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die steuert, wie das Speicherobjekt relativ zum Datenstrom erstellt werden soll. Die Standardeinstellung ist STGSTRM_RESET, die dem Speicherobjekt schreibgeschützten Zugriff gewährt und an Position 0 des Datenstroms startet. Die folgenden Flags können in beliebiger Kombination festgelegt werden, außer wie erwähnt:
    
STGSTRM_CREATE 
  
> Erstellt ein neues Speicherobjekt für das Stream-Objekt. Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist. 
    
STGSTRM_CURRENT 
  
> Startet den Speicher an der aktuellen Position des Datenstroms. Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist. 
    
STGSTRM_MODIFY 
  
> Ermöglicht dem aufrufenden Dienstanbieter das Schreiben in den zurückgegebenen Speicher. Dieses Flag kann nicht festgelegt werden, wenn STGSTRM_RESET festgelegt ist. 
    
STGSTRM_RESET 
  
> Startet den Speicher an Position 0. Dieses Flag kann nicht festgelegt werden, wenn ein anderes Flag festgelegt ist. 
    
 _lppStorageOut_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene **IStorage-Objekt.** 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachrichtenspeicheranbieter unterstützen die **HrIStorageFromStream-Funktion** mithilfe der **IStorage-Schnittstelle** für Anlagen. Store müssen die **IStream-Schnittstelle** implementieren. **HrIStorageFromStream** stellt die **IStorage-Schnittstelle** für das **IStream-Objekt** bereit. Es ist möglich, entweder ein **ILockBytes** oder eine **IStream-Schnittstelle** in _lpUnkIn zu übergeben._ 
  

