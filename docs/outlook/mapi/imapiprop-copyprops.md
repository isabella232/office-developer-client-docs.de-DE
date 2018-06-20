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
ms.openlocfilehash: ff8f13a1dcf678e1d05b6e8e083597156422b83d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792291"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Betrifft**: Outlook 
  
Kopiert oder verschiebt ausgewählten Eigenschaften. 
  
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
  
> [in] Ein Zeiger auf ein Array-Eigenschaft Tag, der angibt, die Eigenschaften zum Kopieren oder verschieben. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kann nicht in das Array aufgenommen werden. Der Parameter _LpIncludeProps_ darf nicht **null**sein.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung der eine Statusanzeige. Wenn **null** in der _LpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle darstellt, die Zugriff auf das Objekt, auf das durch den Parameter _LpDestObj_ verwendet werden muss. Der Parameter _LpInterface_ darf nicht **null**sein.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyProps** die [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufgerufen, um die Kopie zu behandeln oder verschoben wird, muss er stattdessen direkt mit den Fehlerwert MAPI_E_DECLINE_COPY zurückgeben. Das Flag MAPI_DECLINE_OK wird von MAPI festgelegt, um Rekursion zu begrenzen. Clients stellen Sie dieses Flag keine. 
    
MAPI_DIALOG 
  
> Eine Statusanzeige angezeigt.
    
MAPI_MOVE 
  
> **CopyProps** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt. Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** durch einen Kopiervorgang. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls **null**, was bedeutet, dass es keine Notwendigkeit Fehlerinformationen besteht. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Anzeigenamen, durch die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) definiert im Zielobjekt bereits vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Ausführen des Vorgangs kopieren oder verschieben direkt oder indirekt Quellobjekt enthält Zielobjekt. Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die Schnittstelle, die vom _LpInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.
    
Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **CopyProps**zurückgegeben werden soll. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und **CopyProps** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **CopyProps** nur Unicode unterstützt. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht vom Anrufer erwartet.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::CopyProps** -Methode kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt. **CopyProps** dient hauptsächlich zum Beantworten und Weiterleiten von Nachrichten, wobei nur einige der Eigenschaften aus der ursprünglichen Nachricht mit der Antwort Reisen oder Kopie weitergeleitet. 
  
Alle Unterobjekte im Quellobjekt werden vollständig unabhängig von der Verwendung von Eigenschaften, die durch die Struktur [SPropTagArray](sproptagarray.md) angegeben automatisch bei der Konflikte enthalten und kopiert oder verschoben. Standardmäßig überschreibt **CopyProps** Eigenschaften im Zielobjekt, die Eigenschaften aus dem Quellobjekt entsprechen. Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung **CopyProps** bereit oder verlassen sich auf die Implementierung, die MAPI in dessen Support-Objekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::DoCopyProps** -Methode. Wenn Sie führen Sie die Verarbeitung für **DoCopyProps** delegieren, und Sie das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Anruf an den Support und zurückzugeben Sie MAPI_E_DECLINE_COPY stattdessen. Sie können dieses Flag MAPI, um die möglichen Rekursion zu vermeiden, die auftreten können, wenn Sie den Ordner kopieren aufgerufen werden. 
  
Da der Kopiervorgang langen sein kann, sollte eine Statusanzeige angezeigt werden. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die in den _LpProgress_ -Parameter übergeben wird, sofern vorhanden. Wenn _LpProgress_ **null**ist, rufen Sie die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um die MAPI-Implementierung verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie die Kennzeichen MAPI_DECLINE_OK nicht; Es wird in die Anrufe von MAPI verwendet, auf Speicher-Anbieter **CopyProps** Implementierungen message. 
  
Da verschieben und kopieren können Zeit in Anspruch nehmen, es ist ratsam, die Anzeige einer Statusanzeige anfordern, indem Sie das MAPI_DIALOG-Flag. Sie können den Parameter _LpProgress_ festlegen, die Implementierung von **IMAPIProgress**, falls vorhanden, oder **null**. Wenn _LpProgress_ **null**ist, wird **CopyProps** die Standard-Statusanzeige bereitgestellt von MAPI verwendet. 
  
Sie können die Anzeige einer Statusanzeige installieren, indem Sie das Flag MAPI_DIALOG nicht festgelegt. **CopyProps** die Parameter _UlUIParam_ und _LpProgress_ ignoriert und das Symbol anzeigen vermeiden. 
  
 **CopyProps** können melden, globale und einzelne-Fehler oder einen oder mehrere der Eigenschaften auftretenden Fehler. Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt. Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie **null**, anstatt einen gültigen Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters. Wenn **CopyProps** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyProps** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben. Rufen Sie stattdessen die [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **CopyProps** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Wenn Sie Eigenschaften, die für den Objekttyp Quelle eindeutig sind kopieren, müssen Sie sicherstellen, dass das Zielobjekt des gleichen Typs ist. **CopyProps** verhindert nicht, dass Sie Eigenschaften, die um einen Objekttyp mit einem anderen Typ des Objekts in der Regel gehören, zuordnen. Zum Schluss kommen zum Kopieren von Eigenschaften, die für Zielobjekt sinnvoll ist. Beispielsweise sollten Sie eine Adressbuchcontainer nicht Nachrichteneigenschaften kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren möchten, prüfen Sie, ob das Quell- und Ziel-Objekt den gleichen Typ, entweder durch Vergleichen Objektzeigern oder die [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode aufrufen. Legen Sie die Schnittstelle-ID auf den _LpInterface_ der standard-Benutzeroberfläche für das Quellobjekt. Stellen Sie außerdem sicher, dass der Objekttyp oder **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie aus einer Nachricht kopieren möchten, legen Sie _LpInterface_ IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte MAPI_MESSAGE fest. 
  
Wenn ein ungültiger Zeiger im _LpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Um eine Nachricht Empfängerliste zu kopieren, rufen Sie die Nachricht **CopyProps** -Methode, und fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im Array Tag-Eigenschaft. Um die e-Mail-Anlagen zu kopieren, umfassen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft. 
  
Um einen Ordner oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu kopieren, unter anderem **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) Eigenschaften in der Tag-Array-Eigenschaft. Einen Ordner zugeordneten Inhaltstabelle aufnehmen möchten, fügen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft im Array. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::CopyProps** -Methode, um benannte Eigenschaften von einer Nachricht in eine andere kopiert.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::CopyProps** -Methode, um eine Eigenschaft einzufügen, die von einem anderen Objekt kopiert wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagContainerContents-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische PidTagContainerHierarchy-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische PidTagDisplayName-Eigenschaft](pidtagdisplayname-canonical-property.md)
  
[Kanonische PidTagFolderAssociatedContents-Eigenschaft](pidtagfolderassociatedcontents-canonical-property.md)
  
[Kanonische PidTagMessageAttachments-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische PidTagMessageRecipients-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische PidTagObjectType-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

