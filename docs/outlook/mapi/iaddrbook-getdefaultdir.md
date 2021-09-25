---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2604bcc57332b85b631f3ffc1ef46c909e11261
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616838"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner für den anfänglichen Adressbuchcontainer zurück.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEntryID"_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner des Standardcontainers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintragsbezeichner des Standardcontainers wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Clientanwendungen und Dienstanbieter rufen die **GetDefaultDir-Methode** auf, um den Eintragsbezeichner des Standardadressbuchcontainers abzurufen. Der Standardcontainer wird dem Benutzer beim ersten Öffnen des Adressbuchs im Adressbuch angezeigt. Wenn ein Standardcontainer nicht durch einen Aufruf der [IAddrBook::SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) festgelegt wurde, weist MAPI als Standardcontainer den ersten Container mit Namen zu, bei denen es sich nicht um das persönliche Adressbuch (PAB) handelt. Wenn ein solcher Container nicht gefunden werden kann, wird das PAB zum Standardcontainer. 
  
Um das Standardverzeichnis festzulegen, ruft ein Client oder Anbieter die **SetDefaultDir-Methode** auf. Clients und Anbieter müssen die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) nicht aufrufen. da Änderungen am Adressbuch nicht durchgeführt werden, werden änderungen sofort dauerhaft vorgenommen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI verwendet die **GetDefaultDir-Methode,** um die ID für den Standardadressbuchcontainer abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

