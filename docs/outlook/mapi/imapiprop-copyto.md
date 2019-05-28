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
  
Kopiert oder verschiebt alle Eigenschaften, außer speziell ausgeschlossene Eigenschaften.
  
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
  
> in Die Anzahl der Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden sollen.
    
 _rgiidExclude_
  
> in Ein Array von Schnittstellen Bezeichnern (IIDs), die Schnittstellen angeben, die nicht verwendet werden sollen, wenn zusätzliche Informationen kopiert oder in das Zielobjekt verschoben werden.
    
 _lpExcludeProps_
  
> in Ein Zeiger auf ein Eigenschaften-Tag-Array, das die Eigenschaftentags identifiziert, die aus dem Kopier-oder Verschiebevorgang ausgeschlossen werden sollen. Die Übergabe von **null** im _lpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **CopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues** -Element der [SPropProblemArray](spropproblemarray.md) -Struktur, auf das _lpExcludeProps_ verweist, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> in Ein Zeiger auf eine Statusindikator Implementierung. Wenn **null** im _lpProgress_ -Parameter übergeben wird, stellt MAPI die Status Implementierung bereit. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet wird, auf das durch den _lpDestObj_ -Parameter verwiesen wird. Der _lpInterface_ -Parameter darf nicht **null**sein.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske mit Flags, die den Kopier-oder Verschiebevorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DECLINE_OK 
  
> Wenn **CopyTo** die [IMAPISupport::D ocopyto](imapisupport-docopyto.md) -Methode zum Verarbeiten des Kopier-oder Verschiebevorgangs aufruft, sollte stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden. Das MAPI_DECLINE_OK-Flag wird von MAPI festgelegt, um die Rekursion zu begrenzen. Clients legen dieses Flag nicht fest. 
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> In **CopyTo** sollte anstelle eines Kopiervorgangs ein Verschiebevorgang ausgeführt werden. Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt dürfen nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine **SPropProblemArray** -Struktur; andernfalls **null**, was darauf hinweist, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger bei der Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Ein SubObject kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Anzeigenamen, der durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft angegeben ist, bereits im Zielobjekt vorhanden ist. 
    
MAPI_E_DECLINE_COPY 
  
> Der Dienstanbieter implementiert den Kopiervorgang nicht.
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt, das den Kopier-oder Verschiebevorgang ausführt, enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde erhebliche Arbeit ausgeführt, bevor diese Bedingung erkannt wurde, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyTo**. Die folgenden Fehler gelten für eine einzelne Eigenschaft:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyTo** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht gravierend; der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Typ der Eigenschaft ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Hinweise

Standardmäßig kopiert oder verschiebt die **IMAPIProp:: CopyTo** -Methode alle Eigenschaften des aktuellen Objekts in ein Zielobjekt. **CopyTo** wird verwendet, wenn ein Objekt exakt kopiert oder verschoben werden soll, wobei alle oder die meisten seiner Eigenschaften intakt sind. 
  
Alle unter Objekte im Source-Objekt werden automatisch in die Operation aufgenommen und in ihrer Gesamtheit kopiert oder verschoben. Standardmäßig überschreibt **CopyTo** alle Eigenschaften im Zielobjekt, die Eigenschaften des Quellobjekts entsprechen. Wenn bereits eine der kopierten oder verschobenen Eigenschaften im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften durch die neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unberührt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie können eine vollständige Implementierung von **CopyTo** bereitstellen oder sich auf die Implementierung verlassen, die von MAPI im Unterstützungsobjekt bereitgestellt wird. Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::D ocopyto**auf. Wenn Sie die Verarbeitung jedoch an **DoCopyTo** delegieren und Sie das MAPI_DECLINE_OK-Flag übergeben, vermeiden Sie stattdessen den Support-und den Return-MAPI_E_DECLINE_COPY. MAPI wird mit diesem Flag aufgerufen, um die mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann. 
  
Da der Kopiervorgang langwierig sein kann, sollten Sie eine Statusanzeige anzeigen. Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die im _lpProgress_ -Parameter übergeben wird (sofern vorhanden). Wenn _lpProgress_ den Wert **null**aufweist, rufen Sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode auf, um die MAPI-Implementierung zu verwenden. 
  
Versuchen Sie nicht, im Zielobjekt bekannte schreibgeschützte Eigenschaften festzulegen; Geben Sie stattdessen MAPI_E_NO_ACCESS zurück.
  
Die Quell-und Zielobjekte sollten dieselben Schnittstellen verwenden. Gibt MAPI_E_INVALID_PARAMETER zurück, wenn _lpInterface_ nicht festgelegt ist. 
  
Gibt MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannten Schnittstellen ausgeschlossen werden.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das MAPI_DECLINE_OK-Flag nicht fest; MAPI verwendet es in den Aufrufen von Implementierungen des Nachrichtenspeicher Anbieters **CopyTo** . 
  
Da Kopier-und Verschiebevorgänge Zeit in Anspruch nehmen können, sollten Sie die Anzeige einer Statusanzeige anfordern, indem Sie das MAPI_DIALOG-Flag festlegen. Sie können den _lpProgress_ -Parameter auf die Implementierung von **IMAPIProgress**, wenn Sie einen haben, oder auf **null**festlegen. Wenn _lpProgress_ **null**ist, verwendet **CopyTo** den Standardstatus Indikator, der von MAPI bereitgestellt wird. 
  
Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG-Flag nicht festlegen. Die Parameter _ulUIParam_ und _lpProgress_ werden von **CopyTo** ignoriert, und das Symbol wird nicht angezeigt. 
  
 **CopyTo** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in einer **SPropProblemArray** -Struktur gespeichert. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie für den Property Problem Array structure-Parameter anstelle eines gültigen Zeigers einen **null**-Wert übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **CopyTo** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **CopyTo** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray** -Struktur zurückgegeben. Rufen Sie stattdessen [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) auf, um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **CopyTo** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray** -Struktur frei, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt vom gleichen Typ ist. Durch **CopyTo** wird nicht verhindert, dass Sie Eigenschaften zuordnen, die normalerweise zu einem Objekttyp gehören, und einen anderen Objekttyp aufweisen. Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind. Beispielsweise sollten Sie keine Nachrichteneigenschaften in einen Adressbuchcontainer kopieren. 
  
Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell-und das Zielobjekt vom gleichen Typ sind, indem Sie entweder Objektzeiger vergleichen oder [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)aufrufen. Legen Sie den Schnittstellenbezeichner, auf den _lpInterface_ verweist, auf die Standardschnittstelle für das Source-Objekt fest. Stellen Sie außerdem sicher, dass der Objekttyp oder die **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist. Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE fest. 
  
Wenn ein ungültiger Zeiger im _lpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar. 
  
Das Ausschließen von Eigenschaften für einen **CopyTo** -Aufruf kann hilfreich sein. Einige Objekte weisen beispielsweise Eigenschaften auf, die für eine einzelne Instanz des Objekts spezifisch sind, beispielsweise das Datum und die Uhrzeit der Nachrichtenzustellung. Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md)) im Property-Tag Exclude-Array an. Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft zum Exclude-Array hinzu. Um Anlagen einer Nachricht auszuschließen, fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft zum Array hinzu.
  
Ebenso verhindern Sie das Kopieren oder Verschieben einer Hierarchie-oder Inhaltstabelle eines Ordners oder Adressbuch Containers durch Einschließen von **PR_CONTAINER_HIERARCHY** ([pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) im Property-Tag Exclude-Array.
  
Wenn Sie Eigenschaften aus dem Kopier-oder Verschiebevorgang ausschließen möchten, schließen Sie Ihre Eigenschaftentags in den _lpExcludeProps_ -Parameter ein. Wenn Sie die Ergebnisse des **PROP_TAG** -Makros übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Property-Tag-Array zu erstellen, werden alle Eigenschaften mit dieser ID ausgeschlossen. Der folgende Eintrag im Property-Tag-Array bewirkt beispielsweise, dass alle Eigenschaften mit einem Bezeichner von 0x8002, unabhängig vom Typ, ausgeschlossen werden: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Das **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md))-Eigenschaftentag kann nicht im _lpExcludeProps_ -Array enthalten sein. 
  
Die Nützlichkeit des **CopyTo** -Features zum Ausschließen von Schnittstellen ist vielleicht nicht so offensichtlich wie der Nutzen des Ausschließens von Eigenschaften. Sie können eine Schnittstelle ausschließen, wenn Sie zu einem Objekt kopieren, das keine Kenntnis einer Gruppe von Eigenschaften aufweist. Wenn Sie beispielsweise Eigenschaften aus einem Ordner in eine Anlage kopieren, sind die einzigen Eigenschaften, mit denen die Anlage arbeiten kann, die allgemeinen Eigenschaften, die für eine beliebige [IMAPIProp](imapipropiunknown.md) -Implementierung verfügbar sind. Durch das Ausschließen von [IMAPIFolder](imapifolderimapicontainer.md) aus dem Kopiervorgang erhält die Anlage keine spezifischeren Ordner Eigenschaften. 
  
Wenn Sie den _rgiidExclude_ -Parameter verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Beispielsweise bewirkt das Ausschließen von [IMAPIContainer](imapicontainerimapiprop.md) , dass Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen werden. Schließen Sie **IMAPIProp** oder [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) nicht aus, da so viele Schnittstellen von diesen abgeleitet werden. 
  
Ignorieren Sie MAPI_E_COMPUTED-Fehler, die in der **SPropProblemArray** -Struktur im _lppProblems_ -Parameter zurückgegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |LoadFromMSG  <br/> |MfcMapi verwendet die **IMAPIProp:: CopyTo** -Methode, um Eigenschaften aus einer msg-Datei in ein [IMAPIMessageSite](imapimessagesiteiunknown.md) -Objekt zu kopieren.  <br/> |
|FolderDlg. cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MfcMapi verwendet die **IMAPIProp:: CopyTo** -Methode zum Kopieren von Eigenschaften aus einer Quellnachricht in eine Zielnachricht während eines Einfügevorgangs.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische pidtagmessagedeliverytime (-Eigenschaft](pidtagmessagedeliverytime-canonical-property.md)
  
[Kanonische pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[Kanonische pidtagobjecttype (-Eigenschaft](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

