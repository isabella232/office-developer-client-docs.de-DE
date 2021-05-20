---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436762"
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
  
> [in] Der Typ des zu erstellende Ordners. Die folgenden Kennzeichen können festgelegt werden:
    
FOLDER_GENERIC 
  
> Es sollte ein generischer Ordner erstellt werden.
    
FOLDER_SEARCH 
  
> Es sollte ein Suchergebnisordner erstellt werden.
    
 _lpszFolderName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält. Dieser Name ist die Grundlage für die PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) des neuen Ordners.
    
 _lpszFolderComment_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die einen Kommentar enthält, der dem neuen Ordner zugeordnet ist. Diese Zeichenfolge wird zum Wert der eigenschaft **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) des neuen Ordners. Wenn NULL übergeben wird, hat der Ordner keinen anfänglichen Kommentar.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf den neuen Ordner verwendet werden soll. Durch Übergeben von NULL gibt der Nachrichtenspeicheranbieter die Standardordnerschnittstelle [IMAPIFolder : IMAPIContainer zurück.](imapifolderimapicontainer.md) Clients müssen NULL übergeben. Andere Aufrufer können den  _lpInterface-Parameter_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Ordner erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **createFolder,** erfolgreich zurückzukehren, möglicherweise bevor der neue Ordner vollständig für den aufrufenden Client verfügbar ist. Wenn der neue Ordner nicht verfügbar ist, kann ein nachfolgender Aufruf einen Fehler verursachen. 
    
MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich der Ordnername im ANSI-Format.
    
OPEN_IF_EXISTS 
  
> Ermöglicht der Methode einen Erfolg, auch wenn der im  _lpszFolderName-Parameter_ genannte Ordner bereits vorhanden ist, indem der vorhandene Ordner mit diesem Namen geöffnet wird. Beachten Sie, dass Nachrichtenspeicheranbieter, die gleichgeordnete Ordner mit demselben Namen zulassen, möglicherweise keinen vorhandenen Ordner öffnen, wenn mehrere Ordner mit dem angegebenen Namen vorhanden sind. 
    
 _lppFolder_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn OPEN_IF_EXISTS festgelegt ist.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Ein Ordner mit dem im  _lpszFolderName-Parameter angegebenen Namen_ ist bereits vorhanden. Ordnernamen müssen eindeutig sein. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CreateFolder-Methode** erstellt einen Unterordner im aktuellen Ordner und weist dem neuen Ordner einen Eintragsbezeichner zu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateFolder zurückgegeben** wird, beachten Sie, dass die Eintrags-ID für den neuen Ordner möglicherweise nicht verfügbar ist. Einige Nachrichtenspeicheranbieter stellen eintragsbezeichner erst zur Verfügung, nachdem Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Ordners aufgerufen haben, um ihn dauerhaft zu speichern. Dies gilt insbesondere, wenn Sie das MAPI_DEFERRED_ERRORS festgelegt haben. 
  
Beachten Sie, dass einige Nachrichtenspeicheranbieter den  _lppFolder-Parameter_ immer auf die Standardschnittstelle des Ordners verweisen, unabhängig vom Wert, den Sie für den  _lpInterface-Parameter_ übergeben. Da der zurückgegebene Schnittstellenzeiger möglicherweise nicht den von Ihnen erwarteten Typ hat, rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des neuen Ordners auf, um die **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft abzurufen. Falls erforderlich, werfen Sie den Zeiger auf einen geeigneteren Typ, bevor Sie andere Aufrufe machen.
  
Die meisten Nachrichtenspeicheranbieter erfordern, dass der Name des neuen Ordners in Bezug auf die Namen der gleichgeordneten Ordner eindeutig ist. Sie können den Fehlerwert MAPI_E_COLLISION, der zurückgegeben wird, wenn diese Regel nicht befolgt wird. 
  
Um den Eintragsbezeichner des neu erstellten Ordners zu bestimmen, rufen Sie die **IMAPIProp::GetProps-Methode** des neuen Ordners auf, um die PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) **-Eigenschaft** abzurufen.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI verwendet die **CMsgStoreDlg::OnCreateSubFolder-Methode,** um neue Ordner in MFCMAPI zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

