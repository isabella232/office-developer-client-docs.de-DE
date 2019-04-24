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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
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
  
> in Ein Zeiger auf ein Property-Tag-Array, das die Eigenschaften angibt, die kopiert oder verschoben werden sollen. **PR_NULL** ([Pidtagnull (](pidtagnull-canonical-property.md)) kann nicht im Array enthalten sein. Der _lpIncludeProps_ -Parameter darf nicht **null**sein.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> in Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn **null** im _lpProgress_ -Parameter übergeben wird, wird die STATUSanzeige mithilfe der MAPI-Implementierung angezeigt. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden muss, auf das durch den _lpDestObj_ -Parameter verwiesen wird. Der _lpInterface_ -Parameter darf nicht **null**sein.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyProps** die [IMAPISupport::D-ocopyprops](imapisupport-docopyprops.md) -Methode zum Verarbeiten des Kopier-oder Verschiebungsvorgangs aufruft, sollte stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK-Flag wird durch MAPI festgelegt, um die Rekursion einzuschränken. Clients legen dieses Flag nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyProps** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen. Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls **null**, was darauf hinweist, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Subobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen, der durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft definiert ist, bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt, das den Kopier-oder Verschiebungsvorgang ausführt, enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyProps** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp:: CopyProps** -Methode kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt. **CopyProps** wird hauptsächlich zum beantworten und Weiterleiten von Nachrichten verwendet, wobei nur einige der Eigenschaften der ursprünglichen Nachricht mit der Antwort oder der weitergeleiteten Kopie Reisen. 
  
Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang eingeschlossen und vollständig kopiert oder verschoben, unabhängig von der Verwendung von Eigenschaften, die in der [SPropTagArray](sproptagarray.md) -Struktur angegeben sind. Standardmäßig überschreibt **CopyProps** alle Eigenschaften im Zielobjekt, die Eigenschaften des Source-Objekts erfüllen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleiben unberührt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyProps** bereitstellen oder sich auf die Implementierung verlassen, die MAPI im Unterstützungsobjekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::D ocopyprops** -Methode auf. Wenn Sie jedoch die Verarbeitung an **DoCopyProps** delegieren und das MAPI_DECLINE_OK-Flag übergeben werden, vermeiden Sie den Support Aufruf, und geben Sie stattdessen MAPI_E_DECLINE_COPY zurück. Sie werden mit dieser Kennzeichnung von MAPI aufgerufen, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang langwierig sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die im _lpProgress_ -Parameter übergeben wird, sofern vorhanden. Wenn _lpProgress_ ist ****, rufen sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode auf, um die MAPI-Implementierung zu verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK-Flag nicht fest; Sie wird von MAPI in ihren Aufrufen von **CopyProps** -Implementierungen des Nachrichtenspeicher Anbieters verwendet. 
  
Da Kopier-und Verschiebungsvorgänge Zeit in Anspruch nehmen können, ist es ratsam, eine Statusanzeige anzufordern, indem Sie das MAPI_DIALOG-Flag festlegen. Sie können den Parameter _lpProgress_ auf die Implementierung von **IMAPIProgress**festlegen, sofern vorhanden, oder auf **null**. Wenn _lpProgress_ ist ****, verwendet **CopyProps** die Standard Fortschrittsanzeige von MAPI. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG-Flag nicht festlegen. **CopyProps** ignoriert die Parameter _ulUIParam_ und _lpProgress_ und verhindert die Anzeige des Indikators. 
  
 **CopyProps** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt. Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie **null**anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschafts Problem übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **COPYPROPS** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **COPYPROPS** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ aufweist. **CopyProps** verhindert nicht, dass Sie Eigenschaften zuordnen, die normalerweise zu einem Objekttyp mit einem anderen Objekttyp gehören. Sie müssen die Eigenschaften kopieren, die für das Zielobjekt sinnvoll sind. Sie sollten beispielsweise keine Nachrichteneigenschaften in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell-und Zielobjekt derselbe Typ ist, indem Sie entweder Objektzeiger vergleichen oder die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode aufrufen. Legen Sie die Schnittstellenkennung, auf die von _lpInterface_ verwiesen wird, auf die Standardschnittstelle für das Source-Objekt fest. Stellen Sie außerdem sicher, dass die Eigenschaft Objekttyp oder **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE. 
  
Wenn ein ungültiger Zeiger im _lpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Um die Empfängerliste einer Nachricht zu kopieren, rufen Sie die **CopyProps** -Methode der Nachricht auf, und schließen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft in das Tag-Array der Eigenschaft ein. Schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft ein, um die Anlagen der Nachricht zu kopieren. 
  
Wenn Sie die Hierarchie-oder Inhaltstabelle eines Ordner-oder Adressbuch Containers kopieren möchten, schließen Sie die Eigenschaften **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) in das Array für Property-Tags. Schließen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in das Array ein, um die zugeordnete Inhaltstabelle eines Ordners einzuschließen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp:: CopyProps** -Methode, um benannte Eigenschaften aus einer Nachricht in eine andere zu kopieren.  <br/> |
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: onPasteproperty  <br/> |MFCMAPI verwendet die **IMAPIProp:: CopyProps** -Methode, um eine Eigenschaft einzufügen, die aus einem anderen Objekt kopiert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische Pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische Pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische Pidtagfolderassociatedcontents (-Eigenschaft](pidtagfolderassociatedcontents-canonical-property.md)
  
[Kanonische Pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische Pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische Pidtagobjecttype (-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

