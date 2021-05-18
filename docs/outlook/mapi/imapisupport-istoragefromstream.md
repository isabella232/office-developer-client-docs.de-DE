---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316587"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Implementiert ein Speicherobjekt für den Zugriff auf einen Datenstrom.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parameter

 _lpUnkIn_
  
> [in] Ein Zeiger auf ein Streamobjekt.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den Datenstrom verwendet werden soll, auf den _lpUnkIn verweist._ Jeder der folgenden Werte ist gültig: IID_IStream, IID_ILockBytes oder **Null**, was angibt, dass die [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) für den Zugriff auf den Datenstrom verwendet werden soll. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Speicherobjekt relativ zum Streamobjekt erstellt werden soll. Standardmäßig wird der Speicher mit schreibgeschützten Zugriff erstellt, und der Datenstrom beginnt an Position 0 im Speicher. Die folgenden Kennzeichen können festgelegt werden:
    
STGSTRM_CREATE 
  
> Ein neues Speicherobjekt sollte für das Streamobjekt erstellt werden.
    
STGSTRM_CURRENT 
  
> Das Speicherobjekt sollte an der aktuellen Position des Datenstroms beginnen.
    
STGSTRM_MODIFY 
  
> Der Aufrufer sollte über Lese-/Schreibberechtigungen für das zurückgegebene Speicherobjekt verfügen.
    
STGSTRM_RESET 
  
> Das Speicherobjekt sollte an Position 0 beginnen.
    
 _lppStorageOut_
  
> [out] Ein Zeiger auf einen Zeiger auf das Speicherobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Speicherobjekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::IStorageFromStream-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **IStorageFromStream auf,** um ein Speicherobjekt zum Öffnen bestimmter Eigenschaften zu erstellen. Dienstanbieter, die über eine eigene Implementierung der [IStorage-Schnittstelle](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) verfügen, müssen **IStorageFromStream nicht aufrufen.** 
  
Das von **IStorageFromStream** erstellte Speicherobjekt ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) des Datenstroms auf, um die Referenzanzahl zu erhöhen und die Anzahl dann zu dekrementieren, wenn der Speicher freigegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) eines Ihrer Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage-Schnittstelle** zu öffnen, führen Sie die folgenden Aufgaben aus: 
  
1. Öffnen Sie ein Stream-Objekt mit Lese-/Schreibberechtigung für die Eigenschaft.
    
2. Markieren Sie den Eigenschaftendatenstrom intern als Speicherobjekt.
    
3. Rufen **Sie IStorageFromStream auf,** um ein Speicherobjekt zu generieren. 
    
4. Gibt einen Zeiger auf dieses Speicherobjekt zurück.
    
Wenn Sie zusätzliche Schnittstellen implementieren, die das Speicherobjekt verwenden, erstellen Sie ein Objekt, das das Speicherobjekt umschließt, und implementieren Sie eine [höhere IUnknown::QueryInterface-Methode.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) 
  
Lassen Sie nicht zu, dass eine Eigenschaft mit der **IStream-Schnittstelle** geöffnet wird, wenn sie mit **IStorage erstellt wurde.** Lassen Sie dagegen nicht zu, dass eine Eigenschaft mit der **IStorage-Schnittstelle** geöffnet wird, wenn sie mit **IStream erstellt wurde.** 
  
Mit einer Ausnahme ist es akzeptabel, die **IStreamDocfile-Schnittstelle** zum Streamen eines Speicherobjekts von einem Container in einen anderen zu verwenden, aber der IID_IStreamDocfile-Schnittstellenbezeichner muss im _lpInterface-Parameter_ der **OpenProperty-Methode** übergeben werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

