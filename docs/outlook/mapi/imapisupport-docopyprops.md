---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c5a2de3e74e17e6d6d2250c148a9a865ada9d0db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596085"
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
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt mit den zu kopierenden oder zu verschiebenden Eigenschaften verwendet werden soll.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das die zu kopierenden oder zu verschiebenden Eigenschaften enthält.
    
 _lpIncludeProps_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein gezähltes Array von Eigenschaftstags enthält, die die zu kopierenden oder zu verschiebenden Eigenschaften angeben. Der  _LpIncludeProps-Parameter_ darf nicht NULL sein. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn NULL im  _lpProgress-Parameter_ übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner, der die Schnittstelle darstellt, die verwendet werden soll, um auf das Objekt zuzugreifen, um die Eigenschaften zu empfangen, die kopiert oder verschoben werden.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **DoCopyProps** sollte einen Verschiebungsvorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Kennzeichen nicht festgelegt ist, führt **DoCopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine zu kopierende oder zu verschiebende Eigenschaft ist bereits im Zielobjekt vorhanden, und das flag MAPI_NOREPLACE festgelegt ist. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt enthält das Zielobjekt direkt oder indirekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise umfangreiche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird vom Quellobjekt nicht unterstützt, oder die vom  _lpDestInterface-Parameter identifizierte_ Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyProps.** Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **DoCopyProps** unterstützt keinen Unicode- oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der Typ, den der Aufrufer erwartet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::D oCopyProps-Methode** wird für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **DoCopyProps** aufrufen, um die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) für ihre Ordner und Nachrichten zu implementieren. **DoCopyProps** kopiert oder verschiebt die Eigenschaften, die im Eigenschaftentagarray identifiziert werden, auf das von  _lpIncludeProps_ verwiesen wird und die in dem Objekt vorhanden sind, auf das von  _lpSrcObj_ verwiesen wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie Eigenschaften zwischen Objekten desselben Typs kopieren, z. B. zwei Meldungen, müssen die Parameter  _lpSrcInterface_ und  _lpDestInterface_ denselben Schnittstellenbezeichner enthalten, und die Parameter  _lpSrcObj_ und  _lpDestObj_ müssen auf Objekte desselben Typs verweisen. Wenn  _lpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER zurück. Wenn Sie  _lpDestInterface_ auf einen akzeptablen Schnittstellenbezeichner festlegen,  _lpDestObj_ jedoch auf einen ungültigen Zeiger festlegen, sind die Ergebnisse unvorhersehbar. Höchstwahrscheinlich schlägt Ihr Anbieter fehl. 
  
Legen Sie das flag MAPI_NOREPLACE fest, wenn keine der Eigenschaften im Zielobjekt überschrieben werden soll. Eigenschaften im Zielobjekt, die im Quellobjekt vorhanden sind und nicht überschrieben werden, werden nicht gelöscht oder geändert.
  
Um die Empfängerliste einer Nachricht zu kopieren, schließen Sie die **eigenschaft PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) in das Eigenschaftentagarray ein, auf das der  _Parameter lpIncludeProps_ verweist. Um die Anlagen der Nachricht zu kopieren, schließen Sie die **Eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ein. 
  
Um die Hierarchie oder das Inhaltsverzeichnis eines Ordners oder Adressbuchcontainers zu kopieren, schließen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftentagarray ein. Um die zugeordnete Inhaltstabelle eines Ordners einzuschließen, fügen Sie die **eigenschaft PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) in das Array ein.
  
Wenn Unterordner kopiert oder verschoben werden, werden deren Inhalte vollständig kopiert oder verschoben, unabhängig von der Verwendung der durch die **SPropTagArray-Struktur** angegebenen Eigenschaften. 
  
 **DoCopyProps** meldet globale Fehler, die bei dem gesamten Vorgang auftreten, und einzelne Fehler, die mit einer oder mehreren der Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray-Struktur** eingefügt. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Arraystrukturparameter des Eigenschaftsproblems übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _Parameter "lppProblems"._ Wenn **DoCopyProps** S_OK zurückgibt, überprüfen Sie mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray-Struktur** keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DoCopyProps** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
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

