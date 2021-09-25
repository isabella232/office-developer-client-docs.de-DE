---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 04cce495a0149b77429467eb814c5b7a6960dd2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575848"
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
  
> [in] Ein Zeiger auf ein Datenstromobjekt.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Stream verwendet werden soll, auf den von  _lpUnkIn_ verwiesen wird. Jeder der folgenden Werte ist gültig: IID_IStream, IID_ILockBytes oder **NULL**, was angibt, dass die [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) für den Zugriff auf den Datenstrom verwendet werden soll. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Speicherobjekt relativ zum Datenstromobjekt erstellt werden soll. Standardmäßig wird der Speicher mit schreibgeschütztem Zugriff erstellt, und der Datenstrom beginnt bei Position 0 im Speicher. Die folgenden Flags können festgelegt werden:
    
STGSTRM_CREATE 
  
> Für das Streamobjekt sollte ein neues Speicherobjekt erstellt werden.
    
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::IStorageFromStream-Methode** wird für alle Dienstanbieter-Supportobjekte implementiert. Dienstanbieter rufen **IStorageFromStream** auf, um ein Speicherobjekt zum Öffnen bestimmter Eigenschaften zu erstellen. Dienstanbieter, die über eine eigene Implementierung der [IStorage-Schnittstelle](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) verfügen, müssen **IStorageFromStream** nicht aufrufen. 
  
Das von **IStorageFromStream** erstellte Speicherobjekt ruft die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) des Streams auf, um die Referenzanzahl zu erhöhen, und verringert dann die Anzahl, wenn der Speicher freigegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) eines Ihrer Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage-Schnittstelle** zu öffnen, führen Sie die folgenden Aufgaben aus: 
  
1. Öffnen Sie ein Stream-Objekt mit Lese-/Schreibberechtigung für die Eigenschaft.
    
2. Kennzeichnen Sie den Eigenschaftendatenstrom intern als Speicherobjekt.
    
3. Rufen Sie **IStorageFromStream** auf, um ein Speicherobjekt zu generieren. 
    
4. Gibt einen Zeiger auf dieses Speicherobjekt zurück.
    
Wenn Sie zusätzliche Schnittstellen implementieren, die das Speicherobjekt verwenden, erstellen Sie ein Objekt, das das Speicherobjekt umschließt, und implementieren Sie eine [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) auf höherer Ebene. 
  
Lassen Sie nicht zu, dass eine Eigenschaft mit der **IStream-Schnittstelle** geöffnet wird, wenn sie mit **IStorage** erstellt wurde. Lassen Sie dagegen nicht zu, dass eine Eigenschaft mit der **IStorage-Schnittstelle** geöffnet wird, wenn sie mit **IStream** erstellt wurde. 
  
Mit einer Ausnahme kann die **IStreamDocfile-Schnittstelle** verwendet werden, um ein Speicherobjekt von einem Container in einen anderen zu streamen, aber der IID_IStreamDocfile Schnittstellenbezeichner muss im _lpInterface-Parameter_ der **OpenProperty-Methode** übergeben werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

