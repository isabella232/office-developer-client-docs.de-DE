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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792272"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Betrifft**: Outlook 
  
Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme von speziell Ausgeschlossene Eigenschaften.
  
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
  
> [in] Die Anzahl der Schnittstellen zum ausschließen, wenn Eigenschaften kopiert oder verschoben werden.
    
 _rgiidExclude_
  
> [in] Ein Array von Schnittstellenbezeichner (IIDs), die Schnittstellen, die nicht verwendet werden soll angibt, wenn zusätzliche Informationen kopiert oder und Zielobjekt verschoben.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf einen Tag Array-Eigenschaft, die die Eigenschaftentags identifiziert, die von der Kopie ausgeschlossen werden soll oder verschoben wird. Übergeben von **null** in der _LpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden soll. **CopyTo** gibt zurück, dass MAPI_E_INVALID_PARAMETER, wenn das **cValues** Mitglied der [SPropProblemArray](spropproblemarray.md) -Struktur mit _LpExcludeProps_ gezeigt auf 0 gesetzt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung der Fortschritt-Symbol. Wenn **null** in der _LpProgress_ -Parameter übergeben wird, wird die Implementierung des Fortschritts von MAPI bereitgestellt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellenbezeichner (IID), der die Schnittstelle für verwendet werden, um Zugriff auf das Objekt, durch den Parameter _LpDestObj_ auf darstellt. Der Parameter _LpInterface_ darf nicht **null**sein.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyTo** die [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) -Methode aufgerufen, um die Kopie zu behandeln oder verschoben wird, muss er stattdessen direkt mit den Fehlerwert MAPI_E_DECLINE_COPY zurückgeben. Das Flag MAPI_DECLINE_OK wird von MAPI festgelegt, um Rekursion zu begrenzen. Clients stellen Sie dieses Flag keine. 
    
MAPI_DIALOG 
  
> Eine Statusanzeige angezeigt.
    
MAPI_MOVE 
  
> **CopyTo** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt. Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** durch einen Kopiervorgang. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, wird die **CopyTo** vorhandene Eigenschaften überschrieben. 
    
 _lppProblems_
  
> [in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine **SPropProblemArray** -Struktur. andernfalls **null**, gibt an, keine Notwendigkeit zur Fehlerinformationen. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaften haben erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Namen anzeigen – von der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft angegebenen – im Zielobjekt bereits vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Ausführen des Vorgangs kopieren oder verschieben direkt oder indirekt Quellobjekt enthält Zielobjekt. Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die Schnittstelle, die vom _LpInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.
    
Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **CopyTo**zurückgegeben werden soll. Die folgenden Fehler gelten für eine einzelne Eigenschaft:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und **CopyTo** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **CopyTo** nur Unicode unterstützt. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht vom Anrufer erwartet.
    
## <a name="remarks"></a>Hinweise

Standardmäßig wird die **IMAPIProp::CopyTo** -Methode kopiert oder verschiebt alle Eigenschaften des aktuellen Objekts ein Zielobjekt. **CopyTo** wird verwendet, wenn ein Objekt kopiert oder genau mit der gesamten oder die meisten ihrer Eigenschaften intakt verschoben werden soll. 
  
Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und kopiert oder vollständig verschoben. Standardmäßig wird die **CopyTo** Eigenschaften im Zielobjekt, die Eigenschaften aus dem Quellobjekt entsprechen überschrieben. Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können bieten eine vollständige Implementierung der **CopyTo** oder verlassen sich auf die Implementierung, die MAPI in dessen Support-Objekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::DoCopyTo**. Wenn Sie führen Sie die Verarbeitung für **DoCopyTo** delegieren, und Sie das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Anruf an den Support und zurückzugeben Sie MAPI_E_DECLINE_COPY stattdessen. MAPI wird Aufrufen dieses Flag die mögliche Rekursion zu vermeiden, die auftreten können, wenn Ordner kopiert werden. 
  
Da der Kopiervorgang langen sein kann, sollte eine Statusanzeige angezeigt werden. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die in den _LpProgress_ -Parameter übergeben, sofern vorhanden. Wenn _LpProgress_ **null**ist, rufen Sie die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um die MAPI-Implementierung verwenden. 
  
Versuchen Sie keine bekannten Eigenschaften Read-only im Zielobjekt festgelegt; Geben Sie stattdessen MAPI_E_NO_ACCESS zurück.
  
Die Quell- und Ziel-Objekte sollten die gleichen Schnittstellen verwenden. MAPI_E_INVALID_PARAMETER zurück, wenn _LpInterface_ nicht festgelegt ist. 
  
MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannte Schnittstellen ausgeschlossen werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie die Kennzeichen MAPI_DECLINE_OK nicht; MAPI setzt es seine Anrufe auf Speicher-Anbieter **CopyTo** Implementierungen message. 
  
Da verschieben und kopieren können Zeit in Anspruch nehmen, sollten Sie die Anzeige einer Statusanzeige durch Festlegen des MAPI_DIALOG-Flags anfordern. Sie können den Parameter _LpProgress_ festlegen, die Implementierung von **IMAPIProgress**, falls vorhanden, oder **null**. Wenn _LpProgress_ **null**ist, verwendet **CopyTo** die Standard-Statusanzeige MAPI bietet. 
  
Sie können die Anzeige einer Statusanzeige installieren, indem Sie das Flag MAPI_DIALOG nicht festgelegt. **CopyTo** die Parameter _UlUIParam_ und _LpProgress_ ignoriert und das Symbol wird nicht angezeigt. 
  
 **CopyTo** können melden, globale und einzelne Fehler oder Fehler, die mit einer oder mehrerer Eigenschaften auftreten. Diese einzelnen Fehler befinden sich in einer **SPropProblemArray** Struktur. Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie **null**, anstatt einen gültigen Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters. Wenn **CopyTo** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyTo** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben. Rufen Sie stattdessen [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **CopyTo** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Wenn Sie Eigenschaften, die für den Objekttyp Quelle eindeutig sind kopieren, müssen Sie sicherstellen, dass Zielobjekt des gleichen Typs ist. **CopyTo** verhindert nicht, dass Sie Eigenschaften, die um einen Objekttyp mit einem anderen Typ des Objekts in der Regel gehören, zuordnen. Zum Schluss kommen zum Kopieren von Eigenschaften, die für Zielobjekt sinnvoll ist. Beispielsweise sollten Sie eine Adressbuchcontainer nicht Nachrichteneigenschaften kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren, prüfen Sie, ob das Quell- und Ziel-Objekt den gleichen Typ, entweder durch Vergleichen Objektzeigern oder den Aufruf von [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx). Legen Sie die Schnittstelle-ID auf den _LpInterface_ der standard-Benutzeroberfläche für das Quellobjekt. Darüber hinaus werden Sie sicher, dass der Objekttyp oder **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie aus einer Nachricht kopieren, legen Sie _LpInterface_ IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte MAPI_MESSAGE fest. 
  
Wenn ein ungültiger Zeiger im _LpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Ausschließen von Eigenschaften für einen Anruf **CopyTo** kann hilfreich sein. Beispielsweise haben einige Objekte, Eigenschaften, die für eine einzelne Instanz des Objekts, wie etwa das Datum und die Uhrzeit der Nachrichtenübermittlung spezifisch sind. Geben Sie zum Vermeiden von Zeitaufwands für die Bereitstellung einer Nachricht, wenn Sie die Nachricht auf einen anderen Ordner kopieren, kopieren **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) die Array-Eigenschaft Tag ausschließen. Um eine Nachricht Empfängerliste auszuschließen, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft dem Exclude-Array. Um eine e-Mail-Anlagen auszuschließen, fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft dem Array hinzu.
  
In ähnlicher Weise zu verhindern, dass das Kopieren oder Verschieben eines Ordners oder Adressbuchcontainer des Hierarchie oder Inhalt Tabelle, einschließlich **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in der Eigenschaft Tag Array ausschließen.
  
Ausschließen von Eigenschaften aus der Kopie oder Verschiebevorgang, deren Eigenschaftentags im _LpExcludeProps_ -Parameter enthalten. Wenn Sie die Ergebnisse des Makros **PROP_TAG** zum Erstellen einer Eigenschaftentag aus einem bestimmten Kennzeichen im Array Tag-Eigenschaft übergeben wird, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Der folgende Eintrag im Array Tag-Eigenschaft bewirkt beispielsweise alle Eigenschaften mit der ID 0x8002, ausgeschlossen werden sollen, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Das **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Tag-Eigenschaft kann nicht im Array _LpExcludeProps_ enthalten sein. 
  
Die Nützlichkeit des **CopyTo** Features zum Ausschließen von Schnittstellen ist möglicherweise nicht offensichtlich die Nützlichkeit von Eigenschaften ausschließen. Wenn Sie auf ein Objekt kopieren, die keiner Gruppe von Eigenschaften vorhanden sind, können Sie eine Schnittstelle ausschließen. Wenn Sie Eigenschaften aus einem Ordner in einer Anlage kopieren, sind die einzigen Eigenschaften, mit denen die Anlage zusammenarbeiten kann beispielsweise die generischen Eigenschaften [IMAPIProp](imapipropiunknown.md) Implementierung verfügbar sind. Der Kopiervorgang [IMAPIFolder](imapifolderimapicontainer.md) ausgeschlossen, erhalten die Anlage nicht bestimmte Ordner Eigenschaften. 
  
Wenn Sie den Parameter _RgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle Schnittstellen, die von dieser Schnittstelle abgeleitet ausgeschlossen. Ausschließen von [IMAPIContainer](imapicontainerimapiprop.md) bewirkt beispielsweise, dass Ordner oder Adresse Adressbuch-Container, je nach den Typ des Anbieters ausgeschlossen werden sollen. Schließen Sie keine **IMAPIProp** oder [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , da so viele Schnittstellen, die von ihnen abgeleitet werden. 
  
Ignorieren Sie MAPI_E_COMPUTED Fehler in der Struktur **SPropProblemArray** im _LppProblems_ -Parameter zurückgegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::CopyTo** -Methode, um Eigenschaften aus einer MSG-Datei in ein [IMAPIMessageSite](imapimessagesiteiunknown.md) -Objekt zu kopieren.  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::CopyTo** -Methode, um Eigenschaften aus einer Datenquelle Nachricht in einer Zielnachricht während eines Einfügevorgangs zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagContainerContents-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische PidTagContainerHierarchy-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische PidTagMessageAttachments-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische PidTagMessageDeliveryTime-Eigenschaft](pidtagmessagedeliverytime-canonical-property.md)
  
[Kanonische PidTagMessageRecipients-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische PidTagObjectType-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

