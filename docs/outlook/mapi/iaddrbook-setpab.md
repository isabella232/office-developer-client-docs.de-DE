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
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569302"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt einen bestimmten Container als das persönliche Adressbuch (PAB) fest.
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Containers, als die PAB festgelegt werden sollen. Der Parameter _LpEntryID_ darf nicht NULL sein. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der angegebene Container wurde als PAB eingerichtet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen Sie die **SetPAB** -Methode, um einen bestimmten Container als PAB festzulegen. Die PAB ist ein Container, der Einträge aus anderen Containern sowie neue Einträge kopiert besteht. 
  
Ein Aufruf von **SetPAB** stellt einen Container als PAB her, bis Containers ist nicht verfügbar gemacht, oder ein neuer Container die PAB durch einen nachfolgenden Aufruf von **SetPAB wird**. 
  
Clients und Anbieter müssen nicht Aufrufen der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, damit die Änderung PAB dauerhaft entfernt wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI (engl.) verwendet die **SetPAB** -Methode, um dem angegebenen Container PAB stellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

