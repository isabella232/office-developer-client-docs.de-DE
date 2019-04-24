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
  
Implementiert ein Storage-Objekt, um auf einen Stream zuzugreifen.
  
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
  
> in Ein Zeiger auf ein Stream-Objekt.
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Stream verwendet werden soll, auf den durch _lpUnkIn_verwiesen wird. Jeder der folgenden Werte ist gültig: IID_IStream, IID_ILockBytes oder **null**, der angibt, dass die [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle für den Zugriff auf den Stream verwendet werden soll. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Speicherobjekt relativ zum Stream-Objekt erstellt werden soll. Standardmäßig wird der Speicher mit schreibgeschütztem Zugriff erstellt, und der Datenstrom beginnt bei Position NULL im Speicher. Die folgenden Flags können festgelegt werden:
    
STGSTRM_CREATE 
  
> Für das Stream-Objekt sollte ein neues Storage-Objekt erstellt werden.
    
STGSTRM_CURRENT 
  
> Das Speicherobjekt sollte an der aktuellen Position des Streams beginnen.
    
STGSTRM_MODIFY 
  
> Der Aufrufer sollte über Lese-/Schreibzugriff für das zurückgegebene Speicherobjekt verfügen.
    
STGSTRM_RESET 
  
> Das Speicherobjekt sollte an Position Null beginnen.
    
 _lppStorageOut_
  
> Out Ein Zeiger auf einen Zeiger auf das Speicherobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Speicherobjekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: IStorageFromStream** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **IStorageFromStream** auf, um ein Speicherobjekt zu erstellen, das zum Öffnen bestimmter Eigenschaften verwendet werden soll. Dienstanbieter, die über eine eigene Implementierung der [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) -Schnittstelle verfügen, müssen **IStorageFromStream**nicht aufrufen. 
  
Das von **IStorageFromStream** erstellte Speicherobjekt Ruft die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -Methode des Streams auf, um den Verweiszähler zu erhöhen und dann die Anzahl zu verringern, wenn der Speicher freigegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode eines ihrer Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage** -Schnittstelle zu öffnen, führen Sie die folgenden Aufgaben aus: 
  
1. Öffnen Sie ein Stream-Objekt mit Lese-/Schreibzugriff für die Eigenschaft.
    
2. Kennzeichnen Sie den Stream der Eigenschaft intern als Speicherobjekt.
    
3. Rufen Sie **IStorageFromStream** auf, um ein Speicherobjekt zu generieren. 
    
4. Gibt einen Zeiger auf dieses Speicherobjekt zurück.
    
Wenn Sie zusätzliche Schnittstellen implementieren, die das Storage-Objekt verwenden, erstellen Sie ein Objekt, das das Speicherobjekt umschließt und eine höhere [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) -Methode implementiert. 
  
Lassen Sie eine Eigenschaft nicht mit der **IStream** -Schnittstelle geöffnet werden, wenn Sie mit **IStorage**erstellt wurde. Umgekehrt können Sie eine Eigenschaft nicht mit der **IStorage** -Schnittstelle öffnen, wenn Sie mit **IStream**erstellt wurde. 
  
Mit einer Ausnahme ist es akzeptabel, die **IStreamDocfile** -Schnittstelle zum Streamen eines Speicherobjekts aus einem Container in einen anderen zu verwenden, aber der IID_IStreamDocfile-Schnittstellenbezeichner muss in der LpInterface der **OpenProperty** -Methode übergeben werden. _ _-Parameter. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

