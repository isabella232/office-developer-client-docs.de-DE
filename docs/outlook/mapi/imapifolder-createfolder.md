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
  
> in Der Typ des zu erstellende Ordners. Die folgenden Flags können festgelegt werden:
    
FOLDER_GENERIC 
  
> Es sollte ein generischer Ordner erstellt werden.
    
FOLDER_SEARCH 
  
> Es sollte ein Ordner mit Suchergebnissen erstellt werden.
    
 _lpszFolderName_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält. Dieser Name ist die Basis für die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des neuen Ordners.
    
 _lpszFolderComment_
  
> in Ein Zeiger auf eine Zeichenfolge, die einen Kommentar enthält, der dem neuen Ordner zugeordnet ist. Diese Zeichenfolge wird zum Wert der **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))-Eigenschaft des neuen Ordners. Wenn NULL übergeben wird, hat der Ordner keinen anfänglichen Kommentar.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den neuen Ordner verwendet werden soll. Die Übergabe von NULL bewirkt, dass der Nachrichtenspeicher Anbieter die Standardordner Schnittstelle [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)zurückgibt. Clients müssen NULL überschreiten. Andere Aufrufer können den _lpInterface_ -Parameter auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festlegen. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Erstellung des Ordners steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** , dass CreateFolder erfolgreich zurückgegeben wird, möglicherweise bevor der neue Ordner vollständig für den aufrufenden Client verfügbar ist. Wenn der neue Ordner nicht verfügbar ist, kann der nachfolgende Aufruf zu einem Fehler führen. 
    
MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist der Ordnername im ANSI-Format.
    
OPEN_IF_EXISTS 
  
> Die Methode kann auch dann erfolgreich ausgeführt werden, wenn der im _lpszFolderName_ -Parameter genannte Ordner bereits vorhanden ist, indem der vorhandene Ordner mit diesem Namen geöffnet wird. Beachten Sie, dass Nachrichtenspeicher Anbieter, die gleichgeordnete Ordner mit demselben Namen zulassen, möglicherweise keinen vorhandenen Ordner öffnen, wenn mehrere mit dem angegebenen Namen vorhanden sind. 
    
 _lppFolder_
  
> Out Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn das OPEN_IF_EXISTS-Flag festgelegt ist.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Ein Ordner mit dem im _lpszFolderName_ -Parameter angegebenen Namen ist bereits vorhanden. Ordnernamen müssen eindeutig sein. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: CreateFolder** -Methode erstellt einen Unterordner im aktuellen Ordner und weist dem neuen Ordner eine Eintrags-ID zu. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateFolder** zurückgegeben wird, müssen Sie beachten, dass die Eintrags-ID für den neuen Ordner möglicherweise nicht verfügbar ist. Einige Nachrichtenspeicher Anbieter stellen keine Eingabe-IDs zur Verfügung, bis Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Ordners aufgerufen haben, um Sie dauerhaft zu speichern. Dies gilt insbesondere, wenn Sie das MAPI_DEFERRED_ERRORS-Flag festgelegt haben. 
  
Beachten Sie, dass einige Nachrichtenspeicher Anbieter den Parameter _lppFolder_ immer auf die Standardschnittstelle des Ordners verweisen, unabhängig davon, welcher Wert für den _lpInterface_ -Parameter übergeben wird. Da der zurückgegebene Schnittstellenzeiger möglicherweise nicht vom erwarteten Typ ist, rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des neuen Ordners auf, um die **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md))-Eigenschaft abzurufen. Falls erforderlich, werfen Sie den Zeiger in einen besser geeigneten Typ, bevor Sie andere Aufrufe ausführen.
  
Für die meisten Nachrichtenspeicher Anbieter muss der Name des neuen Ordners im Hinblick auf die Namen seiner nebengeordneten Ordner eindeutig sein. Sie können den MAPI_E_COLLISION-Fehlerwert behandeln, der zurückgegeben wird, wenn diese Regel nicht befolgt wird. 
  
Um die Eintrags-ID des neu erstellten Ordners zu bestimmen, rufen Sie die **IMAPIProp::** GetProps-Methode des neuen Ordners auf, um die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft abzurufen.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnCreateSubFolder  <br/> |MFCMAPI verwendet die **CMsgStoreDlg:: OnCreateSubFolder** -Methode, um neue Ordner in MfcMapi zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

