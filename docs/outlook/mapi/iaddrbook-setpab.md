---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424616"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestimmt einen bestimmten Container als persönliches Adressbuch (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, der als PAB festgelegt werden soll. Der  _lpEntryID-Parameter_ darf nicht NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Container wurde als PAB eingerichtet.
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **SetPAB-Methode** auf, um einen bestimmten Container als PAB zu bestimmen. Das PAB ist ein Container, der aus Einträgen besteht, die aus anderen Containern kopiert wurden, sowie aus neuen Einträgen. 
  
Ein Aufruf von **SetPAB** richtet einen Container als PAB ein, bis dieser Container nicht verfügbar gemacht wird oder ein neuer Container durch einen nachfolgenden Aufruf von **SetPAB** zum PAB wird. 
  
Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) nicht aufrufen, um die PAB-Änderung dauerhaft zu machen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI verwendet die **SetPAB-Methode,** um den angegebenen Container zum PAB zu machen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

