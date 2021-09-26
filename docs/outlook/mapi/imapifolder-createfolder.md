---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41590cc2968c919afac714c348beda8a653f81ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610650"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen neuen Unterordner.
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>Parameter

 _ulFolderType_
  
> [in] Der Typ des zu erstellenden Ordners. Die folgenden Flags können festgelegt werden:
    
FOLDER_GENERIC 
  
> Ein generischer Ordner sollte erstellt werden.
    
FOLDER_SEARCH 
  
> Es sollte ein Suchergebnisordner erstellt werden.
    
 _lpszFolderName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält. Dieser Name ist die Basis für die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft des neuen Ordners.
    
 _lpszFolderComment_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die einen Kommentar enthält, der dem neuen Ordner zugeordnet ist. Diese Zeichenfolge wird zum Wert der **eigenschaft PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) des neuen Ordners. Wenn NULL übergeben wird, hat der Ordner keinen anfänglichen Kommentar.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den neuen Ordner verwendet werden soll. Wenn NULL übergeben wird, gibt der Nachrichtenspeicheranbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)zurück. Clients müssen NULL übergeben. Andere Aufrufer können den  _parameter lpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Ordner erstellt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **CreateFolder** die erfolgreiche Rückgabe, möglicherweise bevor der neue Ordner für den aufrufenden Client vollständig verfügbar ist. Wenn der neue Ordner nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_UNICODE 
  
> Der Name des Ordners hat das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, hat der Ordnername das ANSI-Format.
    
OPEN_IF_EXISTS 
  
> Die Methode kann auch dann erfolgreich ausgeführt werden, wenn der im  _LpszFolderName-Parameter_ genannte Ordner bereits vorhanden ist, indem der vorhandene Ordner mit diesem Namen geöffnet wird. Beachten Sie, dass Nachrichtenspeicheranbieter, die zulassen, dass gleichgeordnete Ordner denselben Namen haben, möglicherweise keinen vorhandenen Ordner öffnen, wenn mehrere Ordner mit dem angegebenen Namen vorhanden sind. 
    
 _lppFolder_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn das flag OPEN_IF_EXISTS festgelegt ist.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Ein Ordner mit dem im  _Parameter lpszFolderName angegebenen_ Namen ist bereits vorhanden. Ordnernamen müssen eindeutig sein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::CreateFolder-Methode** erstellt einen Unterordner im aktuellen Ordner und weist dem neuen Ordner einen Eintragsbezeichner zu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beachten Sie bei der **Rückgabe von CreateFolder,** dass der Eintragsbezeichner für den neuen Ordner möglicherweise nicht verfügbar ist. Einige Nachrichtenspeicheranbieter stellen Eintragsbezeichner erst zur Verfügung, nachdem Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Ordners aufgerufen haben, um sie dauerhaft zu speichern. Dies gilt insbesondere, wenn Sie das MAPI_DEFERRED_ERRORS-Flag festgelegt haben. 
  
Beachten Sie, dass einige Nachrichtenspeicheranbieter den  _lppFolder-Parameter_ immer auf die Standardschnittstelle des Ordners verweisen, unabhängig vom Wert, den Sie für den  _lpInterface-Parameter_ übergeben. Da der zurückgegebene Schnittstellenzeiger möglicherweise nicht dem erwarteten Typ entspricht, rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des neuen Ordners auf, um die **eigenschaft PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) abzurufen. Wandeln Sie den Zeiger ggf. in einen geeigneteren Typ um, bevor Sie andere Aufrufe ausführen.
  
Die meisten Nachrichtenspeicheranbieter erfordern, dass der Name des neuen Ordners in Bezug auf die Namen seiner gleichgeordneten Ordner eindeutig ist. Sie können den MAPI_E_COLLISION Fehlerwert behandeln, der zurückgegeben wird, wenn diese Regel nicht befolgt wird. 
  
Um den Eintragsbezeichner des neu erstellten Ordners zu ermitteln, rufen Sie die **IMAPIProp::GetProps-Methode** des neuen Ordners auf, um die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft abzurufen.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI verwendet die **CMsgStoreDlg::OnCreateSubFolder-Methode,** um neue Ordner in MFCMAPI zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

