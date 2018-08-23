---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a9f0fac76f06bd638aeff89ff096507209cc0287
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568455"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt die Eintrags-ID für die anfängliche Adressbuchcontainer zurück.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID der Standardcontainer.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eintrags-ID der Standardcontainer wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen und Dienstanbieter rufen Sie die **GetDefaultDir** -Methode, um die Eintrags-ID der Standard-Adressbuchcontainer abzurufen. Der standardmäßige Container ist, was der Benutzer erhält im Adressbuch angezeigt wird, wenn das Adressbuch zum ersten Mal geöffnet wird. Wenn ein Standardcontainer nicht durch einen Aufruf an die [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode festgelegt wurde, weist MAPI als Standardcontainer den ersten Container mit Namen, der nicht das persönliche Adressbuch (PAB) ist. Wenn ein solcher Container nicht gefunden werden kann, wird die PAB Standardcontainer. 
  
Wenn Sie die Standardeinstellung festlegen Directory, ein Client oder Anbieter die **SetDefaultDir** -Methode aufgerufen. Clients und Anbieter müssen nicht die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufrufen. Da Änderungen an dem Adressbuch nicht durchgeführt werden, werden sofort permanent geändert. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI (engl.) verwendet die **GetDefaultDir** -Methode, um die ID für die Standard-Adressbuchcontainer erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

