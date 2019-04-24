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
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356392"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme der explizit ausgeschlossenen Eigenschaften.
  
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
  
> in Die Anzahl von Schnittstellen, die ausgeschlossen werden sollen, wenn Eigenschaften kopiert oder verschoben werden.
    
 _rgiidExclude_
  
> in Ein Array von Schnittstellen Bezeichnern (IIDs), die Schnittstellen angeben, die nicht verwendet werden sollen, wenn zusätzliche Informationen in das Zielobjekt kopiert oder verschoben werden.
    
 _lpExcludeProps_
  
> in Ein Zeiger auf ein Property-Tag-Array, das die Eigenschaftentags identifiziert, die vom Kopier-oder Verschiebungsvorgang ausgeschlossen werden sollen. Das übergeben von **null** im _lpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **CopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues** -Element der [SPropProblemArray](spropproblemarray.md) -Struktur, auf die durch _lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> in Ein Zeiger auf eine Statusindikator-Implementierung. Wenn **null** im _lpProgress_ -Parameter übergeben wird, stellt MAPI die Status Implementierung bereit. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das durch den _lpDestObj_ -Parameter verwiesen wird. Der _lpInterface_ -Parameter darf nicht **null**sein.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyTo** die [IMAPISupport::D ocopyto](imapisupport-docopyto.md) -Methode zum Verarbeiten des Kopier-oder Verschiebungsvorgangs aufruft, sollte Sie sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK-Flag wird durch MAPI festgelegt, um die Rekursion einzuschränken. Clients legen dieses Flag nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **CopyTo** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen. Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine **SPropProblemArray** -Struktur; andernfalls **null**, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein Subobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen, der durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft angegeben ist, bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt, das den Kopier-oder Verschiebungsvorgang ausführt, enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyTo**. Die folgenden Fehler gelten für eine einzelne Eigenschaft:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyTo** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Bemerkungen

Standardmäßig kopiert oder verschiebt die **IMAPIProp:: CopyTo** -Methode alle Eigenschaften des aktuellen Objekts in ein Zielobjekt. **CopyTo** wird verwendet, wenn ein Objekt genau kopiert oder verschoben werden soll, wobei alle oder die meisten seiner Eigenschaften intakt sind. 
  
Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang eingeschlossen und werden vollständig kopiert oder verschoben. Standardmäßig überschreibt **CopyTo** alle Eigenschaften im Zielobjekt, die Eigenschaften des Source-Objekts erfüllen. Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleiben unberührt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyTo** bereitstellen oder sich auf die Implementierung verlassen, die MAPI im Unterstützungsobjekt bereitstellt. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::D ocopyto**auf. Wenn Sie jedoch die Verarbeitung an **DoCopyTo** delegieren und das MAPI_DECLINE_OK-Flag übergeben werden, vermeiden Sie den Support Aufruf, und geben Sie stattdessen MAPI_E_DECLINE_COPY zurück. MAPI Ruft mit diesem Flag auf, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang langwierig sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die im _lpProgress_ -Parameter übergeben wird, sofern vorhanden. Wenn _lpProgress_ ist ****, rufen sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode auf, um die MAPI-Implementierung zu verwenden. 
  
Versuchen Sie nicht, alle bekannten schreibgeschützten Eigenschaften im Zielobjekt festzulegen. Geben Sie stattdessen MAPI_E_NO_ACCESS.
  
Die Quell-und Zielobjekte sollten dieselben Schnittstellen verwenden. Geben Sie MAPI_E_INVALID_PARAMETER zurück, wenn _lpInterface_ nicht festgelegt ist. 
  
Geben Sie MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannten Schnittstellen ausgeschlossen sind.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK-Flag nicht fest; MAPI verwendet Sie in ihren Aufrufen der **CopyTo** -Implementierungen des Nachrichtenspeicher Anbieters. 
  
Da Kopier-und Verschiebungsvorgänge Zeit in Anspruch nehmen können, sollten Sie die Anzeige einer Statusanzeige anfordern, indem Sie das MAPI_DIALOG-Flag festlegen. Sie können den Parameter _lpProgress_ auf die Implementierung von **IMAPIProgress**festlegen, sofern vorhanden, oder auf **null**. Wenn _lpProgress_ ist ****, verwendet **CopyTo** den Standardstatus Indikator, der von MAPI bereitgestellt wird. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG-Flag nicht festlegen. **CopyTo** ignoriert die Parameter _ulUIParam_ und _lpProgress_ und zeigt das Symbol nicht an. 
  
 **CopyTo** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur aufgenommen. Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie **null**anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschafts Problem übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **COPYTO** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyTo** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben. Rufen Sie stattdessen [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **COPYTO** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ aufweist. **CopyTo** verhindert nicht, dass Sie Eigenschaften zuordnen, die normalerweise zu einem Objekttyp mit einem anderen Objekttyp gehören. Sie müssen die Eigenschaften kopieren, die für das Zielobjekt sinnvoll sind. Sie sollten beispielsweise keine Nachrichteneigenschaften in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell-und Zielobjekt derselbe Typ ist, indem Sie Objektzeiger vergleichen oder [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)aufrufen. Legen Sie die Schnittstellenkennung, auf die von _lpInterface_ verwiesen wird, auf die Standardschnittstelle für das Source-Objekt fest. Stellen Sie außerdem sicher, dass die Eigenschaft Objekttyp oder **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE. 
  
Wenn ein ungültiger Zeiger im _lpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Das Ausschließen von Eigenschaften für einen **CopyTo** -Aufruf kann hilfreich sein. Einige Objekte haben beispielsweise Eigenschaften, die für eine einzelne Instanz des Objekts spezifisch sind, beispielsweise das Datum und die Uhrzeit der Nachrichtenübermittlung. Um zu verhindern, dass die Übermittlungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md)) im Property-Tag Exclude-Array an. Wenn Sie die Empfängerliste einer Nachricht ausschließen möchten, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft zum Exclude-Array hinzu. Zum Ausschließen der Anlagen einer Nachricht fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft zum Array hinzu.
  
In ähnlicher Weise verhindern Sie das Kopieren oder bewegen einer Ordner-oder Adressbuchcontainer-Hierarchie oder Inhaltstabelle, indem Sie **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) im Property-Tag Exclude-Array.
  
Um Eigenschaften aus dem Kopier-oder Verschiebungsvorgang auszuschließen, schließen Sie deren Eigenschaftstags in den Parameter _lpExcludeProps_ ein. Wenn Sie die Ergebnisse des **PROP_TAG** -Makros zum Erstellen eines Property-Tags aus einem bestimmten Bezeichner im Property-Tag-Array überschreiten, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Beispielsweise bewirkt der folgende Eintrag im Property Tag-Array, dass alle Eigenschaften mit einem Bezeichner von 0x8002 unabhängig vom Typ ausgeschlossen werden: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Das **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md))-Eigenschaftentag kann nicht im _lpExcludeProps_ -Array enthalten sein. 
  
Die Nützlichkeit des **CopyTo** -Features zum Ausschließen von Schnittstellen ist vielleicht nicht so offensichtlich wie die Nützlichkeit des Ausschließens von Eigenschaften. Sie können eine Schnittstelle ausschließen, wenn Sie in ein Objekt kopieren, das über keine Eigenschaftengruppe verfügt. Wenn Sie beispielsweise Eigenschaften aus einem Ordner in eine Anlage kopieren, sind die einzigen Eigenschaften, mit denen die Anlage arbeiten kann, die generischen Eigenschaften, die für jede [IMAPIProp](imapipropiunknown.md) -Implementierung zur Verfügung stehen. Durch das Ausschließen von [IMAPIFolder](imapifolderimapicontainer.md) aus dem Kopiervorgang erhält die Anlage keine spezifischere Ordner Eigenschaften. 
  
Wenn Sie den Parameter _rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Beispielsweise bewirkt das Ausschließen von [IMAPIContainer](imapicontainerimapiprop.md) , dass Ordner oder Adressbuchcontainer abhängig vom Anbietertyp ausgeschlossen werden. Schließen Sie **IMAPIProp** oder [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) nicht aus, da so viele Schnittstellen von Ihnen abgeleitet werden. 
  
Ignoriert MAPI_E_COMPUTED-Fehler, die in der **SPropProblemArray** -Struktur im _lppProblems_ -Parameter zurückgegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI verwendet die **IMAPIProp:: CopyTo** -Methode, um Eigenschaften aus einer msg-Datei in ein [IMAPIMessageSite](imapimessagesiteiunknown.md) -Objekt zu kopieren.  <br/> |
|FolderDlg. cpp  <br/> |CFolderDlg:: HandlePaste  <br/> |MFCMAPI verwendet die **IMAPIProp:: CopyTo** -Methode, um während eines Einfügevorgangs Eigenschaften aus einer Quellnachricht in eine Zielnachricht zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische Pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische Pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische Pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische Pidtagmessagedeliverytime (-Eigenschaft](pidtagmessagedeliverytime-canonical-property.md)
  
[Kanonische Pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische Pidtagobjecttype (-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

