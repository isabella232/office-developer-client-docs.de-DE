---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792012"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**Betrifft**: Outlook 
  
Gibt die Eintrags-ID des Containers, die als das persönliche Adressbuch (PAB) festgelegt ist.
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID des PAB. Der Parameter _LppEntryID_ enthält 0 (null), wenn kein Container als PAB festgelegt wurde. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eintrags-ID des PAB wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Clients rufen Sie die **GetPAB** -Methode, um die Eintrags-ID des Containers als PAB abzurufen. Wenn ein PAB nicht im Profil eingerichtet wurde, wählt MAPI als PAB den ersten Container in der Adressbuchhierarchie, die Änderungen ermöglicht. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI (engl.) wird die **GetPAB** -Methode verwendet, um die ID für das persönliche Adressbuch des Benutzers abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerFlags (kanonische Eigenschaft)](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

