---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356392"
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
  
> [in] Die Anzahl von Schnittstellen, die ausgeschlossen werden sollen, wenn Eigenschaften kopiert oder verschoben werden.
    
 _rgiidExclude_
  
> [in] Ein Array von Schnittstellenbezeichnern (Interface Identifiers, IIDs), die Schnittstellen angeben, die nicht verwendet werden sollten, wenn ergänzende Informationen kopiert oder in das Zielobjekt verschoben werden.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftstags identifiziert, die vom Kopier- oder Verschiebevorgang ausgeschlossen werden sollen. Das Übergeben von **null** im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **CopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn **das cValues-Element** der [SPropProblemArray-Struktur,](spropproblemarray.md) auf die  _von lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Fortschrittsindikatorimplementierung. Wenn **null** im  _lpProgress-Parameter übergeben_ wird, stellt MAPI die Fortschrittsimplementierung. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das der  _lpDestObj-Parameter_ verweist. Der _lpInterface-Parameter_ darf nicht null **sein.**
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyTo** die [IMAPISupport::D oCopyTo-Methode](imapisupport-docopyto.md) aufruft, um den Kopier- oder Verschiebevorgang zu verarbeiten, sollte es stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY. Das MAPI_DECLINE_OK wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Flag nicht festgelegt. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyTo** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine **SPropProblemArray-Struktur;** andernfalls **null**, gibt an, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen – angegeben durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft – bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier- oder Verschiebevorgang direkt oder indirekt ausführen, enthält das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpInterface-Parameter identifizierte_ Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyTo**. Die folgenden Fehler gelten für eine einzelne Eigenschaft:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, **und CopyTo** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, und **CopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>Hinweise

Standardmäßig kopiert oder verschiebt die **IMAPIProp::CopyTo-Methode** alle Eigenschaften des aktuellen Objekts in ein Zielobjekt. **CopyTo** wird verwendet, wenn ein Objekt genau kopiert oder verschoben werden soll, während alle oder die meisten eigenschaften intakt sind. 
  
Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben. Standardmäßig überschreibt **CopyTo** alle Eigenschaften im Zielobjekt, die eigenschaften des Quellobjekts entsprechen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE wird im  _ulFlags-Parameter_ festgelegt. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyTo** bereitstellen oder sich auf die Implementierung verlassen, die MAPI in seinem Supportobjekt bietet. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::D oCopyTo auf.** Wenn Sie jedoch die Verarbeitung an **DoCopyTo** delegieren und das MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Supportaufruf, und geben Sie MAPI_E_DECLINE_COPY zurück. MAPI wird mit diesem Flag aufrufen, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang sehr lang sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie [die IMAPIProgress-Implementierung,](imapiprogressiunknown.md) die im  _lpProgress-Parameter_ übergeben wird, falls eine dieser Implementierungen vor ist. Wenn  _lpProgress_ **null** ist, rufen Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) auf, um die MAPI-Implementierung zu verwenden. 
  
Versuchen Sie nicht, bekannte schreibgeschützte Eigenschaften im Zielobjekt zu setzen. Geben Sie MAPI_E_NO_ACCESS zurück.
  
Die Quell- und Zielobjekte sollten die gleichen Schnittstellen verwenden. Geben MAPI_E_INVALID_PARAMETER zurück,  _wenn lpInterface_ nicht festgelegt ist. 
  
Geben MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannten Schnittstellen ausgeschlossen sind.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das #A0 MAPI_DECLINE_OK. MAPI verwendet es in den Aufrufen von **CopyTo-Implementierungen** des Nachrichtenspeicheranbieters. 
  
Da Kopier- und Verschiebevorgänge einige Zeit in Sich nehmen können, sollten Sie die Anzeige eines Statusindikators anfordern, indem Sie MAPI_DIALOG festlegen. Sie können den  _lpProgress-Parameter_ auf Die Implementierung von **IMAPIProgress** festlegen, wenn Sie über einen verfügen, oder auf **null**. Wenn  _lpProgress_ **null** ist, verwendet **CopyTo** den standardmäßigen Fortschrittsindikator, den MAPI bietet. 
  
Sie können die Anzeige eines Statusindikators unterdrücken, indem Sie das MAPI_DIALOG festlegen. **CopyTo** ignoriert die  _UlUIParam-_ und  _lpProgress-Parameter_ und zeigt den Indikator nicht an. 
  
 **CopyTo** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** platziert. Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie **null** anstelle eines gültigen Zeigers für den Eigenschaftenproblemarraystrukturparameter übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._ Wenn **CopyTo S_OK** zurückgibt, suchen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur. Wenn **CopyTo** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben. Rufen Sie stattdessen [IMAPIProp::GetLastError auf,](imapiprop-getlasterror.md) um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **CopyTo S_OK** zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ hat. **CopyTo** verhindert nicht, dass Sie Eigenschaften, die in der Regel zu einem Objekttyp gehören, einem anderen Objekttyp zuordnen. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie nachrichteneigenschaften nicht in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob quell- und zielobjekt derselbe Typ sind, indem Sie entweder Objektzeiger vergleichen oder [IUnknown::QueryInterface aufrufen.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) Legen Sie den Schnittstellenbezeichner, auf den  _lpInterface verweist,_ auf die Standardschnittstelle für das Quellobjekt. Stellen Sie außerdem sicher, dass der Objekttyp **oder PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie z. B. aus einer Nachricht kopieren, legen  Sie _lpInterface_ auf IID_IMessage und PR_OBJECT_TYPE für beide Objekte MAPI_MESSAGE. 
  
Wenn ein ungültiger Zeiger im  _lpDestObj-Parameter_ übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Das Ausschließen von Eigenschaften bei **einem CopyTo-Aufruf** kann hilfreich sein. Beispielsweise verfügen einige Objekte über Eigenschaften, die für eine einzelne Instanz des Objekts spezifisch sind, z. B. das Datum und die Uhrzeit der Nachrichtenzustellung. Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im #A0 aus. Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie **die PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft zum Exclude-Array hinzu. Zum Ausschließen der Anlagen einer Nachricht fügen Sie **die PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft zum Array hinzu.
  
Verhindern Sie auf ähnliche Weise das Kopieren oder Verschieben der Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers, indem Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das #A0 ausschließen.
  
Um Eigenschaften aus dem Kopier- oder Verschiebevorgang auszuschließen, schließen Sie ihre Eigenschaftstags in den  _lpExcludeProps-Parameter_ ein. Wenn Sie die Ergebnisse  des PROP_TAG übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Der folgende Eintrag im Eigenschaftentagarray bewirkt beispielsweise, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Das **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Eigenschaftstag kann nicht im  _lpExcludeProps-Array enthalten_ sein. 
  
Die Nützlichkeit des **CopyTo-Features** zum Ausschließen von Schnittstellen ist möglicherweise nicht so offensichtlich wie der Nutzen des Ausschließens von Eigenschaften. Sie können eine Schnittstelle ausschließen, wenn Sie in ein Objekt kopieren, das keine Kenntnis einer Gruppe von Eigenschaften hat. Wenn Sie beispielsweise Eigenschaften aus einem Ordner in eine Anlage kopieren, sind die einzigen Eigenschaften, mit der die Anlage arbeiten kann, die generischen Eigenschaften, die mit jeder [IMAPIProp-Implementierung verfügbar](imapipropiunknown.md) sind. Durch Ausschließen [von IMAPIFolder](imapifolderimapicontainer.md) aus dem Kopiervorgang erhält die Anlage keine der spezielleren Ordnereigenschaften. 
  
Wenn Sie den  _Parameter rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Wenn Sie [beispielsweise IMAPIContainer](imapicontainerimapiprop.md) ausschließen, werden Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen. Schließen Sie **IMAPIProp** oder [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) nicht aus, da so viele Schnittstellen von ihnen stammen. 
  
Ignorieren MAPI_E_COMPUTED Fehler, die in der **SPropProblemArray-Struktur** im  _lppProblems-Parameter zurückgegeben_ werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI verwendet die **IMAPIProp::CopyTo-Methode,** um Eigenschaften aus einer MSG-Datei in ein [IMAPIMessageSite-Objekt zu](imapimessagesiteiunknown.md) kopieren.  <br/> |
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
  
[PidTagObjectType (kanonische Eigenschaft)](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

