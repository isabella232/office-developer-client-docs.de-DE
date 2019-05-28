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
  
> in Ein Zeiger auf ein Property-Tag-Array, das die zu kopierende oder zu verschiebende Eigenschaft angibt. **PR_NULL** ([Pidtagnull (](pidtagnull-canonical-property.md)) kann nicht in das Array eingeschlossen werden. Der _lpIncludeProps_ -Parameter darf nicht **null**sein.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> in Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn **null** im _lpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden muss, auf das durch den _lpDestObj_ -Parameter verwiesen wird. Der _lpInterface_ -Parameter darf nicht **null**sein.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske mit Flags, die den Kopier-oder Verschiebevorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyProps** die [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) -Methode zum Verarbeiten des Kopier-oder Verschiebevorgangs aufruft, sollte stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK-Flag wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Flag nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyProps** sollte anstelle eines Kopiervorgangs einen Verschiebevorgang ausführen. Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt dürfen nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, werden vorhandene Eigenschaften von **CopyProps** überschrieben. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls **null**, was darauf hinweist, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger bei der Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein SubObject kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Anzeigenamen, der durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft definiert ist, bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier-oder Verschiebevorgang ausführt, enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde erhebliche Arbeit ausgeführt, bevor diese Bedingung erkannt wurde, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyProps** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht gravierend; der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Typ der Eigenschaft ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Hinweise

Mit der **IMAPIProp:: CopyProps** -Methode werden ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt kopiert oder verschoben. **CopyProps** wird hauptsächlich für das Antworten auf und Weiterleiten von Nachrichten verwendet, bei denen nur einige Eigenschaften aus der ursprünglichen Nachricht mit der Antwort oder weitergeleiteten Kopie Reisen. 
  
Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang aufgenommen und kopiert oder in ihrer Gesamtheit verschoben, unabhängig von der Verwendung von Eigenschaften, die durch die [SPropTagArray](sproptagarray.md) -Struktur angegeben werden. Standardmäßig überschreibt **CopyProps** alle Eigenschaften im Zielobjekt, die Eigenschaften des Quellobjekts entsprechen. Wenn bereits eine der kopierten oder verschobenen Eigenschaften im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften durch die neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unberührt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyProps** bereitstellen oder sich auf die Implementierung verlassen, die von MAPI im Unterstützungsobjekt bereitgestellt wird. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::D ocopyprops** -Methode auf. Wenn Sie die Verarbeitung jedoch an **DoCopyProps** delegieren und Sie das MAPI_DECLINE_OK-Flag übergeben, vermeiden Sie stattdessen den Support-und den Return-MAPI_E_DECLINE_COPY. Sie werden mit dieser Kennzeichnung von MAPI aufgerufen, um die mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang langwierig sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die im _lpProgress_ -Parameter übergeben wird (sofern vorhanden). Wenn _lpProgress_ den Wert **null**aufweist, rufen Sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode auf, um die MAPI-Implementierung zu verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK-Flag nicht fest; Sie wird von MAPI in ihren Aufrufen von **CopyProps** -Implementierungen für Nachrichtenspeicher Anbieter verwendet. 
  
Da Kopier-und Verschiebevorgänge Zeit in Anspruch nehmen können, ist es ratsam, die Anzeige einer Statusanzeige anzufordern, indem das MAPI_DIALOG-Flag festgelegt wird. Sie können den _lpProgress_ -Parameter auf die Implementierung von **IMAPIProgress**, wenn Sie einen haben, oder auf **null**festlegen. Wenn _lpProgress_ den Wert **null**aufweist, verwendet **CopyProps** den Standardstatus Indikator, der von MAPI bereitgestellt wird. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG-Flag nicht festlegen. **CopyProps** ignoriert die Parameter _ulUIParam_ und _lpProgress_ und verhindert, dass der Indikator angezeigt wird. 
  
 **CopyProps** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie für den Property Problem Array structure-Parameter anstelle eines gültigen Zeigers einen **null**-Wert übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **CopyProps** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode auf, um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **CopyProps** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray** -Struktur frei, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt vom gleichen Typ ist. **CopyProps** verhindert nicht, dass Sie Eigenschaften zuordnen, die in der Regel zu einem Objekttyp gehören, mit einem anderen Objekttyp. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie keine Nachrichteneigenschaften in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell-und das Zielobjekt vom gleichen Typ sind, indem Sie entweder Objektzeiger vergleichen oder die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode aufrufen. Legen Sie den Schnittstellenbezeichner, auf den _lpInterface_ verweist, auf die Standardschnittstelle für das Source-Objekt fest. Stellen Sie außerdem sicher, dass der Objekttyp oder die **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE fest. 
  
Wenn ein ungültiger Zeiger im _lpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Wenn Sie die Empfängerliste einer Nachricht kopieren möchten, rufen Sie die **CopyProps** -Methode der Nachricht auf, und fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft in das Property-Tag-Array ein. Um die Anlagen der Nachricht zu kopieren, schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft ein. 
  
Um die Hierarchie-oder Inhaltstabelle eines Ordners oder Adressbuch Containers zu kopieren, schließen Sie die Eigenschaften **PR_CONTAINER_HIERARCHY** ([pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) in das Array von Eigenschaftentags. Schließen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in das Array ein, um die Tabelle zugeordnete Inhalte eines Ordners einzubeziehen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyNamedProps  <br/> |MfcMapi verwendet die **IMAPIProp:: CopyProps** -Methode, um benannte Eigenschaften von einer Nachricht in eine andere zu kopieren.  <br/> |
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: onpasteproperty  <br/> |MfcMapi verwendet die **IMAPIProp:: CopyProps** -Methode, um eine Eigenschaft einzufügen, die aus einem anderen Objekt kopiert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische pidtagfolderassociatedcontents (-Eigenschaft](pidtagfolderassociatedcontents-canonical-property.md)
  
[Kanonische pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische pidtagobjecttype (-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

