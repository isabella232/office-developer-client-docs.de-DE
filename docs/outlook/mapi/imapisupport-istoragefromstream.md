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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a73c87f172b4c97379bb9cd117679d3947c188af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792376"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Betrifft**: Outlook 
  
Zugriff auf einen Datenstrom ein Speicherobjekt implementiert.
  
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
  
> [in] Ein Zeiger auf ein Stream-Objekt.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, für den Zugriff auf das _LpUnkIn_Streams auf darstellt. Eines der folgenden Werte sind gültig: IID_IStream, IID_ILockBytes, oder **null**, gibt an, dass die [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle zum Zugriff auf den Stream verwendet werden soll. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Speicherobjekt ist relativ zu der Stream-Objekt erstellt werden soll. Standardmäßig wird der Speicher mit Schreibschutz erstellt und der Stream beginnt an der Position 0 (null) im Speicher. Die folgenden Kennzeichen können festgelegt werden:
    
STGSTRM_CREATE 
  
> Ein neues Speicherobjekt sollten für das Stream-Objekt erstellt werden.
    
STGSTRM_CURRENT 
  
> Das Speicherobjekt sollte an der aktuellen Position des Datenstroms beginnen.
    
STGSTRM_MODIFY 
  
> Der Aufrufer sollte Lese-/Schreibberechtigung für das zurückgegebene Objekt.
    
STGSTRM_RESET 
  
> Das Speicherobjekt sollte an Position 0 (null) beginnen.
    
 _lppStorageOut_
  
> [out] Ein Zeiger auf einen Zeiger auf das Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::IStorageFromStream** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter Aufrufen **IStorageFromStream** zum Erstellen eines Speicherobjekts für bestimmte Eigenschaften zu öffnen. Dienstanbieter, die ihre eigene Implementierung der Schnittstelle [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) haben, müssen nicht **IStorageFromStream**aufrufen. 
  
Erstelltes **IStorageFromStream** Speicherobjekt ruft der Stream [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) -Methode, um erhöht den Referenzzähler und dann die dekrementiert die Anzahl der, wenn der Speicher freigegeben wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode der Objekte aufgerufen wird, um eine Eigenschaft mit der **IStorage** -Schnittstelle zu öffnen, führen Sie die folgenden Aufgaben aus: 
  
1. Öffnen Sie ein Stream-Objekt mit Lese-/Schreibberechtigung für die Eigenschaft.
    
2. Markieren Sie den Eigenschaftenstream intern als Speicherobjekt.
    
3. Rufen Sie **IStorageFromStream** um ein Speicherobjekt zu generieren. 
    
4. Ein Zeiger auf dieses Speicherobjekt zurückgegeben.
    
Wenn Sie zusätzliche Schnittstellen, die das Objekt verwenden implementieren, erstellen Sie ein Objekt, das das Speicherobjekt umbrochen wird, und Implementieren einer höheren Ebene [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) -Methode. 
  
Lassen Sie keine Eigenschaft mit der **IStream** -Schnittstelle geöffnet werden soll, wenn sie mit **IStorage**erstellt wurde. Lassen Sie eine Eigenschaft mit der **IStorage** -Schnittstelle geöffnet werden soll, wenn sie mit **IStream**erstellt wurde dagegen nicht zu. 
  
Mit einer Ausnahme für die **IStreamDocfile** -Oberfläche verwenden, um ein Speicherobjekt aus einem Container in einen anderen stream akzeptabel ist, aber der IID_IStreamDocfile Schnittstellenbezeichner muss in der **OpenProperty** Methode _übergeben werden LpInterface _Parameter. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

