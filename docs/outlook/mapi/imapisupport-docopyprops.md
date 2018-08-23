---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a30a323874c847d9a08b00512cfd30ff3cf5c5ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591128"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert oder Verschiebt einen oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpSrcInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um Zugriff auf das Objekt mit den Eigenschaften, kopiert oder verschoben werden soll.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das enthält die Eigenschaften kopiert oder verschoben werden soll.
    
 _lpIncludeProps_
  
> [in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein gezählte Eigenschaftentags-Array enthält, die angeben, die Eigenschaften zum Kopieren oder verschieben. Der Parameter _LpIncludeProps_ darf nicht NULL sein. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung der eine Statusanzeige. Wenn NULL in der _LpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstellenbezeichner, der stellt die Schnittstelle dar, die verwendet werden, um Zugriff auf das Objekt, um die Eigenschaften zu erhalten, die kopiert oder verschoben werden.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Eine Statusanzeige angezeigt.
    
MAPI_MOVE 
  
> **DoCopyProps** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt. Wenn dieses Flag nicht festgelegt ist, führt **DoCopyProps** durch einen Kopiervorgang. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, gibt keine Notwendigkeit zur Fehlerinformationen an. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **DoCopyProps** ausführliche Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine Eigenschaft, die kopiert oder verschoben bereits vorhanden ist, im Zielobjekt, und das Flag MAPI_NOREPLACE festgelegt ist. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt enthält direkt oder indirekt Zielobjekt. Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die Schnittstelle, die vom _LpSrcInterface_ -Parameter wird von der Source-Objekt nicht unterstützt, oder die Schnittstelle, die vom _LpDestInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.
    
Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **DoCopyProps**zurückgegeben werden soll. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und **DoCopyProps** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **DoCopyProps** nur Unicode unterstützt. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht den Typ, den der Anrufer erwartet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::DoCopyProps** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht Anbieter können **DoCopyProps** zum Implementieren der [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methode für ihre Ordner und Nachrichten aufrufen. **DoCopyProps** kopiert oder verschiebt die Eigenschaften, die die Tag-Array-Eigenschaft auf den _LpIncludeProps_ erkannt werden, und, die in das Objekt, das auf _LpSrcObj_vorhanden sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Beim Kopieren von Eigenschaften zwischen Objekten des gleichen Typs, wie beispielsweise zwei Nachrichten müssen die Parameter _LpSrcInterface_ und _LpDestInterface_ enthalten die gleichen Bezeichner, und die _LpSrcObj_ und _LpDestObj_ Parameter für die Benutzeroberfläche muss auf Objekte des gleichen Typs zeigen. Wenn _LpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER zurück. Wenn Sie auf eine akzeptable Schnittstellenbezeichner, aber Set _LpDestObj_ in einen ungültigen Zeiger _LpDestInterface_ festlegen, sind die Ergebnisse unvorhersehbar. In den meisten Fällen wird vom Dienstanbieter fehl. 
  
Legen Sie das Flag MAPI_NOREPLACE, wenn Sie nicht möchten, dass alle Eigenschaften im Zielobjekt überschrieben werden soll. Eigenschaften im Zielobjekt, die in der Source-Objekt vorhanden ist und nicht überschrieben werden werden nicht gelöscht oder geändert.
  
Um eine Nachricht Empfängerliste zu kopieren, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft die Tag-Array-Eigenschaft auf den durch den Parameter _LpIncludeProps_ verwiesen. Um die e-Mail-Anlagen zu kopieren, umfassen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft. 
  
Um einen Ordner oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu kopieren, schließen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) im Array Tag-Eigenschaft. Einen Ordner zugeordneten Inhaltstabelle aufnehmen möchten, fügen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft im Array.
  
Wenn Unterordner kopiert oder verschoben werden, werden vollständig unabhängig von der Verwendung von Eigenschaften, die durch die Struktur **SPropTagArray** angegeben deren Inhalt kopiert oder verschoben. 
  
 **DoCopyProps** globale mit dem Vorgang als Ganzes auftretende Fehler und einzelne einen oder mehrere der Eigenschaften auftretenden Fehler gemeldet. Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt. Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie NULL, statt dass ein gültiger Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters. Wenn **DoCopyProps** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyProps** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError](imapisupport-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **DoCopyProps** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagFolderAssociatedContents (kanonische Eigenschaft)](pidtagfolderassociatedcontents-canonical-property.md)
  
[PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

