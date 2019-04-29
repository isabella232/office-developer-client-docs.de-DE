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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436874"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Eintrags-ID für den anfänglichen Adressbuchcontainer zurück.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpcbEntryID_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird. 
    
 _lppEntryID_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID des Standardcontainers.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Eintragsbezeichner des Standardcontainers wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen und Dienstanbieter rufen die **GetDefaultDir** -Methode auf, um den Eintragsbezeichner des Standard Adressbuch Containers abzurufen. Der Standardcontainer ist, was der Benutzer im Adressbuch angezeigt sieht, wenn das Adressbuch zum ersten Mal geöffnet wird. Wenn kein Standardcontainer durch einen Aufruf der [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode festgelegt wurde, weist MAPI als Standardcontainer den ersten Container mit Namen, die nicht das persönliche Adressbuch (PAB) ist. Wenn ein solcher Container nicht gefunden werden kann, wird das PAB zum Standardcontainer. 
  
Zum Festlegen des Standardverzeichnisses Ruft ein Client oder Anbieter die **SetDefaultDir** -Methode auf. Clients und Anbieter müssen die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode nicht aufrufen; Da Änderungen am Adressbuch nicht durchgeführt werden, werden Änderungen sofort dauerhaft vorgenommen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenDefaultDir  <br/> |MFCMAPI verwendet die **GetDefaultDir** -Methode, um die ID für den standardmäßigen Adressbuchcontainer abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische Pidtagcontainerflags (-Eigenschaft](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

