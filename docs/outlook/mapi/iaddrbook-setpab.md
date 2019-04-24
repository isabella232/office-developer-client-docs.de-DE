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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287014"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt einen bestimmten Container als persönliches Adressbuch (PAB) fest.
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Containers, der als PAB festgelegt werden soll. Der _lpEntryID_ -Parameter darf nicht NULL sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angegebene Container wurde als PAB eingerichtet.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **SetPAB** -Methode auf, um einen bestimmten Container als PAB festzulegen. Das PAB ist ein Container, der aus Einträgen aus anderen Containern sowie neuen Einträgen besteht. 
  
Ein Aufruf von **SetPAB** richtet einen Container als PAB ein, bis dieser Container nicht verfügbar gemacht wird oder ein neuer Container durch einen nachfolgenden Aufruf von **SetPAB**zum PAB wird. 
  
Clients und Anbieter müssen nicht die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aufrufen, um das PAB permanent zu ändern. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AbContDlg. cpp  <br/> |CAbContDlg:: OnSetPAB  <br/> |MFCMAPI verwendet die **SetPAB** -Methode, um den angegebenen Container als PAB zu verwenden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Kanonische Pidtagcontainerflags (-Eigenschaft](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

