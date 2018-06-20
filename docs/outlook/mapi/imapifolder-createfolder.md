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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 36fd729b1ca3e5d877d03358d581b83fc6d4782c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792107"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Der Typ des zu erstellenden Ordners. Die folgenden Kennzeichen können festgelegt werden:
    
FOLDER_GENERIC 
  
> Ein generischer Ordner sollte erstellt werden.
    
FOLDER_SEARCH 
  
> Ein Suchergebnisse Ordner sollte erstellt werden.
    
 _lpszFolderName_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen für den neuen Ordner enthält. Dieser Name ist die Grundlage für den neuen Ordner **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft.
    
 _lpszFolderComment_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die einen Kommentar Zusammenhang mit den neuen Ordner enthält. Diese Zeichenfolge wird der Wert der Eigenschaft für den neuen Ordner **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)). Wenn NULL übergeben wird, hat der Ordner keine Kommentar.
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf den neuen Ordner darstellt. Übergeben von NULL wird eine Nachricht an die Standardordner-Schnittstelle zurück, die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Clients müssen NULL übergeben. Andere Aufrufer können den Parameter _LpInterface_ auf IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer oder IID_IMAPIFolder festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Ordner erstellt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die **CreateFolder** erfolgreich, möglicherweise beendet, bevor Sie der neue Ordner vollständig an den aufrufenden Client verfügbar ist. Wenn Sie der neue Ordner nicht verfügbar ist, kann nachfolgende anrufen darauf verursacht einen Fehler. 
    
PARAMETER MAPI_UNICODE 
  
> Der Name des Ordners ist im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist der Name des Ordners im ANSI-Format.
    
OPEN_IF_EXISTS 
  
> Die Methode erfolgreich ausgeführt, auch wenn Sie der Ordner mit dem Namen im Parameter _LpszFolderName_ bereits vorhanden ist, indem Sie den vorhandenen Ordner mit diesem Namen öffnen können. Beachten Sie, dass Nachricht-Anbieter, mit die gleichgeordneten Knoten Ordner, die denselben Namen aufweisen können keinen bestehenden Ordner öffnen möglicherweise, wenn mehr als eine mit dem angegebenen Namen vorhanden ist. 
    
 _lppFolder_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Ordner.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Neue Ordner wurde erfolgreich erstellt oder geöffnet, wenn das Flag OPEN_IF_EXISTS festgelegt ist.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COLLISION 
  
> Ein Ordner mit dem Namen bereits in der _LpszFolderName_ -Parameter angegebenen vorhanden ist. Ordnernamen müssen eindeutig sein. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::CreateFolder** -Methode erstellt einen Unterordner im aktuellen Ordner und den neuen Ordner eine Eintrags-ID zugewiesen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateFolder** zurückgegeben wird, achten Sie darauf, dass die Eintrags-ID für den neuen Ordner möglicherweise nicht verfügbar. Einige Anbieter Nachricht machen nicht Eintragsbezeichner erst verfügbar, nachdem Sie den neuen Ordner [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um sie dauerhaft zu speichern aufgerufen haben. Dies ist insbesondere dann, wenn Sie die Kennzeichen MAPI_DEFERRED_ERRORS eingerichtet haben. 
  
Beachten Sie, dass einige Anbieter Nachricht immer den _LppFolder_ -Parameter auf den Ordner Standardschnittstelle ungeachtet des Werts verweisen, die Sie für den _LpInterface_ -Parameter übergeben. Da Zeiger der Schnittstelle, der zurückgegeben wird nicht vom Typ, die Sie erwarten sein kann, rufen Sie den neuen Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Falls erforderlich, wandeln Sie den Zeiger auf ein anderes besser geeignet, bevor Sie andere Anrufe tätigen.
  
Die meisten Anbieter Nachricht erfordern den Namen des neuen Ordners in Bezug auf die Namen der zugehörigen gleichgeordneten Knoten Ordner eindeutig sein. Möglicherweise den Fehlerwert MAPI_E_COLLISION verarbeitet werden, die zurückgegeben wird, wenn diese Regel nicht befolgt wird. 
  
Um die Eintrags-ID des neu erstellten Ordners zu bestimmen, rufen Sie den neuen Ordner **IMAPIProp::GetProps** -Methode zum Abrufen der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI (engl.) verwendet die **CMsgStoreDlg::OnCreateSubFolder** -Methode zum Erstellen von neuer Ordnern in MFCMAPI (engl.).  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

