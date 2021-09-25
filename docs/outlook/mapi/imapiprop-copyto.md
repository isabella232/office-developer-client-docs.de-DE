---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d4b2f50954e8435f5aa2a3d647eee4486d61d70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584465"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme speziell ausgeschlossener Eigenschaften.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _ciidExclude_
  
> [in] Die Anzahl der Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden sollen.
    
 _rgiidExclude_
  
> [in] Ein Array von Schnittstellenbezeichnern (IIDs), die Schnittstellen angeben, die nicht verwendet werden sollen, wenn ergänzende Informationen in das Zielobjekt kopiert oder verschoben werden.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftentags identifiziert, die vom Kopier- oder Verschiebungsvorgang ausgeschlossen werden sollen. Das Übergeben von **NULL** im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **CopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues-Element** der [SPropProblemArray-Struktur,](spropproblemarray.md) auf die von  _lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn **null** im  _lpProgress-Parameter_ übergeben wird, stellt MAPI die Implementierung des Fortschritts bereit. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das der  _lpDestObj-Parameter_ verweist. Der  _lpInterface-Parameter_ darf nicht **NULL** sein.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyTo** die [IMAPISupport::D oCopyTo-Methode](imapisupport-docopyto.md) aufruft, um den Kopier- oder Verschiebungsvorgang zu verarbeiten, sollte sie stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK Flag wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Kennzeichen nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyTo** sollte einen Verschiebungsvorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Kennzeichen nicht festgelegt ist, führt **CopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Kennzeichen nicht festgelegt ist, überschreibt **CopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine **SPropProblemArray-Struktur;** andernfalls **NULL**, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da im Zielobjekt bereits ein Unterobjekt mit demselben Anzeigenamen ( angegeben durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Kopiervorgang wird vom Dienstanbieter nicht implementiert.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier- oder Verschiebungsvorgang direkt oder indirekt ausführt, enthält das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise umfangreiche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpInterface-Parameter_ identifizierte Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **Struktur SPropProblemArray** zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyTo**. Die folgenden Fehler gelten für eine einzelne Eigenschaft:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyTo** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp entspricht nicht dem Typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Standardmäßig kopiert oder verschiebt die **IMAPIProp::CopyTo-Methode** alle Eigenschaften des aktuellen Objekts in ein Zielobjekt. **CopyTo** wird verwendet, wenn ein Objekt genau kopiert oder verschoben werden soll, wobei alle oder die meisten seiner Eigenschaften intakt sind. 
  
Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben. Standardmäßig überschreibt **CopyTo** alle Eigenschaften im Zielobjekt, die den Eigenschaften des Quellobjekts entsprechen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE im  _ulFlags-Parameter_ festgelegt ist. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyTo** bereitstellen oder sich auf die Implementierung verlassen, die MAPI in ihrem Supportobjekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::D oCopyTo** auf. Wenn Sie jedoch die Verarbeitung an **DoCopyTo** delegieren und das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Supportaufruf und geben stattdessen MAPI_E_DECLINE_COPY zurück. MAPI wird mit diesem Flag aufgerufen, um mögliche Rekursionen zu vermeiden, die beim Kopieren von Ordnern auftreten können. 
  
Da der Kopiervorgang sehr lang sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die im _lpProgress-Parameter_ übergebene [IMAPIProgress-Implementierung,](imapiprogressiunknown.md) falls vorhanden. Wenn  _lpProgress_ **null** ist, rufen Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) auf, um die MAPI-Implementierung zu verwenden. 
  
Versuchen Sie nicht, bekannte schreibgeschützte Eigenschaften im Zielobjekt festzulegen. stattdessen MAPI_E_NO_ACCESS zurückgeben.
  
Die Quell- und Zielobjekte sollten die gleichen Schnittstellen verwenden. Gibt MAPI_E_INVALID_PARAMETER zurück, wenn  _lpInterface_ nicht festgelegt ist. 
  
Gibt MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannten Schnittstellen ausgeschlossen sind.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK Flag nicht fest. DIE MAPI verwendet sie in ihren Aufrufen von **CopyTo-Implementierungen** des Nachrichtenspeicheranbieters. 
  
Da Kopier- und Verschiebungsvorgänge einige Zeit in Anspruch nehmen können, sollten Sie die Anzeige einer Statusanzeige anfordern, indem Sie das flag MAPI_DIALOG festlegen. Sie können den  _parameter lpProgress_ auf Die Implementierung von **IMAPIProgress** festlegen, falls vorhanden, oder auf **NULL**. Wenn  _lpProgress_ **null** ist, verwendet **CopyTo** die standardmäßige Statusanzeige, die MAPI bereitstellt. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG Flag nicht festlegen. **CopyTo** ignoriert die  _Parameter ulUIParam_ und  _lpProgress_ und zeigt den Indikator nicht an. 
  
 **CopyTo** kann globale und einzelne Fehler oder Fehler melden, die bei einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray-Struktur** eingefügt. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie für den Arraystrukturparameter des Eigenschaftsproblems **null** anstelle eines gültigen Zeigers übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _Parameter "lppProblems"._ When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure. Wenn **CopyTo** einen Fehler zurückgibt, werden in der **SPropProblemArray-Struktur** keine Informationen zurückgegeben. Rufen Sie stattdessen [IMAPIProp::GetLastError](imapiprop-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **CopyTo** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ aufweist. **CopyTo** verhindert nicht, dass Sie Eigenschaften, die in der Regel zu einem Objekttyp gehören, einem anderen Objekttyp zuordnen. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie Nachrichteneigenschaften nicht in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren, überprüfen Sie, ob das Quell- und Das Zielobjekt denselben Typ aufweisen, indem Sie entweder Objektzeiger vergleichen oder [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)aufrufen. Legen Sie den Schnittstellenbezeichner, auf den  _lpInterface_ verweist, auf die Standardschnittstelle für das Quellobjekt fest. Stellen Sie außerdem sicher, dass der Objekttyp oder **die PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) -Eigenschaft für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie  _lpInterface_ auf IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE fest. 
  
Wenn im  _LpDestObj-Parameter_ ein ungültiger Zeiger übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Das Ausschließen von Eigenschaften für einen **CopyTo-Aufruf** kann hilfreich sein. Beispielsweise verfügen einige Objekte über Eigenschaften, die für eine einzelne Instanz des Objekts spezifisch sind, z. B. das Datum und die Uhrzeit der Nachrichtenübermittlung. Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im Eigenschaftstag-Ausschlussarray an. Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie die **Eigenschaft PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) zum Ausschlussarray hinzu. Um die Anlagen einer Nachricht auszuschließen, fügen Sie dem Array die **Eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) hinzu.
  
Verhindern Sie auf ähnliche Weise das Kopieren oder Verschieben der Hierarchie oder des Inhaltsverzeichnisses eines Ordners oder Adressbuchcontainers, indem **Sie PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftstag-Ausschlussarray einschließen.
  
Um Eigenschaften vom Kopier- oder Verschiebungsvorgang auszuschließen, schließen Sie deren Eigenschaftentags in den  _Parameter lpExcludeProps_ ein. Wenn Sie die Ergebnisse des **makros PROP_TAG** übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Beispielsweise bewirkt der folgende Eintrag im Eigenschaftentagarray, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Das **eigenschaftstag PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kann nicht in das  _lpExcludeProps-Array_ eingeschlossen werden. 
  
Die Nützlichkeit des **CopyTo-Features** zum Ausschließen von Schnittstellen ist möglicherweise nicht so offensichtlich wie die Nützlichkeit des Ausschließens von Eigenschaften. Sie können eine Schnittstelle ausschließen, wenn Sie in ein Objekt kopieren, das keine Kenntnis von einer Gruppe von Eigenschaften hat. Wenn Sie beispielsweise Eigenschaften aus einem Ordner in eine Anlage kopieren, können die einzigen Eigenschaften, mit denen die Anlage arbeiten kann, die generischen Eigenschaften sein, die mit jeder [IMAPIProp-Implementierung](imapipropiunknown.md) verfügbar sind. Durch Ausschließen von [IMAPIFolder](imapifolderimapicontainer.md) vom Kopiervorgang erhält die Anlage keine der spezifischeren Ordnereigenschaften. 
  
Wenn Sie den  _Parameter "rgiidExclude"_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Das Ausschließen von [IMAPIContainer](imapicontainerimapiprop.md) führt beispielsweise dazu, dass Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen werden. Schließen Sie **IMAPIProp** oder [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) nicht aus, da so viele Schnittstellen von ihnen abgeleitet sind. 
  
Ignorieren Sie MAPI_E_COMPUTED Fehler, die in der **Struktur "SPropProblemArray"** im  _Parameter "lppProblems"_ zurückgegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyTo-Methode,** um Eigenschaften aus einer MSG-Datei in ein [IMAPIMessageSite-Objekt](imapimessagesiteiunknown.md) zu kopieren.  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyTo-Methode,** um Eigenschaften aus einer Quellnachricht während eines Einfügevorgangs in eine Zielnachricht zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime (kanonische Eigenschaft)](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische PidTagObjectType-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

