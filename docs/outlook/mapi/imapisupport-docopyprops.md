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
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405583"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt eine oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.
  
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt mit den Eigenschaften verwendet werden soll, die kopiert oder verschoben werden sollen.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das die eigenschaften enthält, die kopiert oder verschoben werden sollen.
    
 _lpIncludeProps_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein gezähltes Array von Eigenschaftstags enthält, die die Zu kopierenden oder verschiebenden Eigenschaften angeben. Der  _lpIncludeProps-Parameter_ darf nicht NULL sein. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators.
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung eines Fortschrittsindikators. Wenn NULL im  _lpProgress-Parameter_ übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, um die Eigenschaften zu empfangen, die kopiert oder verschoben werden.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **DoCopyProps** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Flag nicht festgelegt ist, **führt DoCopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, **überschreibt DoCopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine zu kopierende oder zu verschobene Eigenschaft ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE ist festgelegt. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt enthält direkt oder indirekt das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die durch den  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird vom Quellobjekt nicht unterstützt, oder die vom  _lpDestInterface-Parameter_ identifizierte Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE festgelegt, und **DoCopyProps** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der Typ, den der Aufrufer erwartet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::D oCopyProps-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **DoCopyProps aufrufen,** um die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) für ihre Ordner und Nachrichten zu implementieren. **DoCopyProps** kopiert oder verschiebt die Eigenschaften, die im Eigenschaftentagarray identifiziert werden, auf das  _lpIncludeProps_ verweist und die im Objekt vorhanden sind, auf das  _von lpSrcObj_ verwiesen wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie Eigenschaften zwischen Objekten desselben Typs kopieren, z. B. zwei Nachrichten, müssen die  _Parameter lpSrcInterface_ und  _lpDestInterface_ denselben Schnittstellenbezeichner enthalten, und die  _Parameter lpSrcObj_ und  _lpDestObj_ müssen auf Objekte desselben Typs verweisen. Wenn  _lpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER. Wenn Sie  _lpDestInterface_ auf einen akzeptablen Schnittstellenbezeichner festlegen,  _aber lpDestObj_ auf einen ungültigen Zeiger festlegen, sind die Ergebnisse unvorhersehbar. Höchstwahrscheinlich wird Ihr Anbieter fehlschlagen. 
  
Legen Sie MAPI_NOREPLACE, wenn keine der Eigenschaften im Zielobjekt überschrieben werden soll. Eigenschaften im Zielobjekt, die im Quellobjekt vorhanden sind und nicht überschrieben werden, werden nicht gelöscht oder geändert.
  
Um die Empfängerliste einer Nachricht **zu** kopieren, schließen Sie die PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft in das Eigenschaftentagarray ein, auf das der  _lpIncludeProps-Parameter_ verweist. Um die Anlagen der Nachricht zu kopieren, schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft ein. 
  
Um die Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers zu kopieren, fügen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftentagarray ein. Um die zugeordnete Inhaltstabelle eines Ordners zu enthalten, schließen Sie **die PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) -Eigenschaft in das Array ein.
  
Wenn Unterordner kopiert oder verschoben werden, werden deren Inhalte vollständig kopiert oder verschoben, unabhängig von der Verwendung von Eigenschaften, die von der **SPropTagArray-Struktur angegeben** werden. 
  
 **DoCopyProps** meldet globale Fehler, die mit dem Gesamten des Vorgangs auftreten, und einzelne Fehler, die bei einer oder mehreren der Eigenschaften auftreten. Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** angezeigt. Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Parameter für die Arraystruktur des Eigenschaftsproblems übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._ Wenn **DoCopyProps** S_OK, überprüfen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyProps** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DoCopyProps** S_OK, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
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

