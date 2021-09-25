---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eef2fef85e40340aa15dd3dc5a4ec2b4e1ac6d8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575876"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt ausgewählte Eigenschaften. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpIncludeProps_
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die zu kopierenden oder zu verschiebenden Eigenschaften angibt. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kann nicht in das Array eingeschlossen werden. Der  _Parameter lpIncludeProps_ darf nicht **NULL** sein.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn **null** im  _lpProgress-Parameter_ übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die verwendet werden muss, um auf das Objekt zuzugreifen, auf das der  _lpDestObj-Parameter_ verweist. Der  _lpInterface-Parameter_ darf nicht **NULL** sein.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyProps** die [IMAPISupport::D oCopyProps-Methode aufruft,](imapisupport-docopyprops.md) um den Kopier- oder Verschiebungsvorgang zu verarbeiten, sollte er stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK Flag wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Kennzeichen nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyProps** sollte einen Verschiebungsvorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Kennzeichen nicht festgelegt ist, führt **CopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls **null**, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da bereits ein Unterobjekt mit demselben Anzeigenamen, definiert durch die **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Kopiervorgang wird vom Dienstanbieter nicht implementiert.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier- oder Verschiebungsvorgang direkt oder indirekt ausführt, enthält das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise umfangreiche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpInterface-Parameter_ identifizierte Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **Struktur SPropProblemArray** zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyProps** unterstützt nicht Unicode, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp entspricht nicht dem Typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::CopyProps-Methode** kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt. **CopyProps** wird hauptsächlich zum Antworten auf und Weiterleiten von Nachrichten verwendet, wobei nur einige Eigenschaften der ursprünglichen Nachricht mit der Antwort oder weitergeleiteten Kopie weitergeleitet werden. 
  
Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und in ihrer Gesamtheit kopiert oder verschoben, unabhängig von der Verwendung der durch die [SPropTagArray-Struktur](sproptagarray.md) angegebenen Eigenschaften. Standardmäßig überschreibt **CopyProps** alle Eigenschaften im Zielobjekt, die den Eigenschaften des Quellobjekts entsprechen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE im  _ulFlags-Parameter_ festgelegt ist. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyProps** bereitstellen oder sich auf die Implementierung verlassen, die MAPI in ihrem Supportobjekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::D oCopyProps-Methode** auf. Wenn Sie jedoch die Verarbeitung an **DoCopyProps** delegieren und das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Supportaufruf und geben stattdessen MAPI_E_DECLINE_COPY zurück. Sie werden mit diesem Flag von MAPI aufgerufen, um mögliche Wiederholungen zu vermeiden, die beim Kopieren von Ordnern auftreten können. 
  
Da der Kopiervorgang sehr lang sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die [IMAPIProgress-Implementierung,](imapiprogressiunknown.md) die im  _lpProgress-Parameter_ übergeben wird, falls vorhanden. Wenn  _lpProgress_ **null** ist, rufen Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) auf, um die MAPI-Implementierung zu verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK Flag nicht fest. sie wird von der MAPI in ihren Aufrufen von **CopyProps-Implementierungen** des Nachrichtenspeicheranbieters verwendet. 
  
Da Kopier- und Verschiebungsvorgänge einige Zeit in Anspruch nehmen können, empfiehlt es sich, die Anzeige einer Statusanzeige anzufordern, indem Sie das MAPI_DIALOG-Kennzeichen festlegen. Sie können den  _parameter lpProgress_ auf Die Implementierung von **IMAPIProgress** festlegen, falls vorhanden, oder auf **NULL**. Wenn  _lpProgress_ **null** ist, verwendet **CopyProps** die standardmäßige Statusanzeige, die von MAPI bereitgestellt wird. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG Flag nicht festlegen. **CopyProps** ignoriert die  _Parameter ulUIParam_ und  _lpProgress_ und verhindert die Anzeige des Indikators. 
  
 **CopyProps** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren der Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray-Struktur** eingefügt. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie für den Arraystrukturparameter des Eigenschaftsproblems **null** anstelle eines gültigen Zeigers übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _Parameter "lppProblems"._ When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure. Wenn **CopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray-Struktur** keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **CopyProps** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ aufweist. **CopyProps** hindert Sie nicht daran, Eigenschaften, die normalerweise zu einem Objekttyp gehören, einem anderen Objekttyp zuzuordnen. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie Nachrichteneigenschaften nicht in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren, überprüfen Sie, ob das Quell- und Das Zielobjekt denselben Typ aufweisen, indem Sie entweder Objektzeiger vergleichen oder die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) aufrufen. Legen Sie den Schnittstellenbezeichner, auf den  _lpInterface_ verweist, auf die Standardschnittstelle für das Quellobjekt fest. Stellen Sie außerdem sicher, dass der Objekttyp oder **die PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) -Eigenschaft für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie  _lpInterface_ auf IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE fest. 
  
Wenn im  _LpDestObj-Parameter_ ein ungültiger Zeiger übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Rufen Sie zum Kopieren der Empfängerliste einer Nachricht die **CopyProps-Methode** der Nachricht auf, und schließen Sie die **Eigenschaft PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) in das Eigenschaftentagarray ein. Um die Anlagen der Nachricht zu kopieren, schließen Sie die **Eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ein. 
  
Um die Hierarchie oder das Inhaltsverzeichnis eines Ordner- oder Adressbuchcontainers zu kopieren, schließen Sie die **Eigenschaften PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftentagarray ein. Um die zugeordnete Inhaltstabelle eines Ordners einzuschließen, fügen Sie die **eigenschaft PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) in das Array ein. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyProps-Methode,** um benannte Eigenschaften aus einer Nachricht in eine andere zu kopieren.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyProps-Methode,** um eine Eigenschaft einzufügen, die aus einem anderen Objekt kopiert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagDisplayName (kanonische Eigenschaft)](pidtagdisplayname-canonical-property.md)
  
[PidTagFolderAssociatedContents (kanonische Eigenschaft)](pidtagfolderassociatedcontents-canonical-property.md)
  
[PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische PidTagObjectType-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

