---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345507"
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
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die zu kopierenden oder zu verschiebenden Eigenschaften angibt. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kann nicht in das Array eingeschlossen werden. Der _lpIncludeProps-Parameter_ darf nicht **null sein.**
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung eines Fortschrittsindikators. Wenn **null** im  _lpProgress-Parameter übergeben_ wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden muss, auf das der  _lpDestObj-Parameter_ verweist. Der _lpInterface-Parameter_ darf nicht null **sein.**
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyProps** die [IMAPISupport::D oCopyProps-Methode](imapisupport-docopyprops.md) aufruft, um den Kopier- oder Verschiebevorgang zu verarbeiten, sollte es stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY. Das MAPI_DECLINE_OK wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Flag nicht festgelegt. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyProps** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls **null**, gibt an, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen, definiert durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft, bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier- oder Verschiebevorgang direkt oder indirekt ausführen, enthält das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpInterface-Parameter identifizierte_ Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, **und CopyProps** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, **und CopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::CopyProps-Methode** kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt. **CopyProps wird** hauptsächlich zum Beantworten und Weiterleiten von Nachrichten verwendet, wobei nur einige der Eigenschaften aus der ursprünglichen Nachricht mit der Antwort oder der weitergeleiteten Kopie reisen. 
  
Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben, unabhängig von der Verwendung von Eigenschaften, die durch die [SPropTagArray-Struktur angegeben](sproptagarray.md) werden. Standardmäßig überschreibt **CopyProps** alle Eigenschaften im Zielobjekt, die den Eigenschaften des Quellobjekts entsprechen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE wird im  _ulFlags-Parameter_ festgelegt. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyProps** bereitstellen oder sich auf die Implementierung verlassen, die MAPI in seinem Supportobjekt bietet. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::D oCopyProps-Methode** auf. Wenn Sie jedoch die Verarbeitung an **DoCopyProps** delegieren und das MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Supportaufruf, und geben Sie MAPI_E_DECLINE_COPY zurück. Sie werden von MAPI mit diesem Flag aufgerufen, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang sehr lang sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie [die IMAPIProgress-Implementierung,](imapiprogressiunknown.md) die im  _lpProgress-Parameter_ übergeben wird, wenn es eine gibt. Wenn  _lpProgress_ **null** ist, rufen Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) auf, um die MAPI-Implementierung zu verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das #A0 MAPI_DECLINE_OK. sie wird von MAPI in den Aufrufen von **CopyProps-Implementierungen** des Nachrichtenspeicheranbieters verwendet. 
  
Da Kopier- und Verschiebevorgänge zeitweise dauern können, sollten Sie die Anzeige eines Statusindikators anfordern, indem Sie MAPI_DIALOG festlegen. Sie können den  _lpProgress-Parameter_ auf Die Implementierung von **IMAPIProgress** festlegen, wenn Sie über einen verfügen, oder auf **null**. Wenn  _lpProgress_ **null ist,** verwendet **CopyProps** die standardmäßige Fortschrittsanzeige, die von MAPI bereitgestellt wird. 
  
Sie können die Anzeige eines Statusindikators unterdrücken, indem Sie das MAPI_DIALOG festlegen. **CopyProps** ignoriert die  _UlUIParam-_ und  _lpProgress-Parameter_ und vermeidet die Anzeige des Indikators. 
  
 **CopyProps kann** globale und einzelne Fehler oder Fehler melden, die bei einer oder mehreren der Eigenschaften auftreten. Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** angezeigt. Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie **null** anstelle eines gültigen Zeigers für den Eigenschaftenproblemarraystrukturparameter übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._ Wenn **CopyProps** S_OK, überprüfen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur. Wenn **CopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray-Struktur keine Informationen** zurückgegeben. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **CopyProps** S_OK, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ hat. **CopyProps** verhindert nicht, dass Sie Eigenschaften, die in der Regel zu einem Objekttyp gehören, einem anderen Objekttyp zuordnen. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie nachrichteneigenschaften nicht in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell- und das Zielobjekt denselben Typ haben, indem Sie entweder Objektzeiger vergleichen oder die [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) aufrufen. Legen Sie den Schnittstellenbezeichner, auf den  _lpInterface verweist,_ auf die Standardschnittstelle für das Quellobjekt. Stellen Sie außerdem sicher, dass der Objekttyp **oder PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und die PR_OBJECT_TYPE für beide Objekte auf MAPI_MESSAGE.  
  
Wenn ein ungültiger Zeiger im  _lpDestObj-Parameter_ übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Rufen Sie zum Kopieren der Empfängerliste einer Nachricht die **CopyProps-Methode** der Nachricht auf, und schließen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft in das Eigenschaftentagarray ein. Um die Anlagen der Nachricht zu kopieren, schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft ein. 
  
Um die Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers zu kopieren, fügen Sie die **Eigenschaften PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftentagarray ein. Um die zugeordnete Inhaltstabelle eines Ordners zu enthalten, schließen Sie **die PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) -Eigenschaft in das Array ein. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyProps-Methode,** um benannte Eigenschaften von einer Nachricht in eine andere zu kopieren.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyProps-Methode** zum Einfügen einer Eigenschaft, die aus einem anderen Objekt kopiert wurde.  <br/> |
   
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
  
[PidTagObjectType (kanonische Eigenschaft)](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

