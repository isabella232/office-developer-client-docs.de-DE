---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5c289b22844cdc3f94c14198d4b010228ee195c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567466"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme ausdrücklich ausgeschlossener Eigenschaften, in ein anderes Objekt.
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _lpSrcInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, das über die zu kopierenden oder zu verschiebenden Eigenschaften verfügt.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das die zu kopierenden oder zu verschiebenden Eigenschaften aufweist.
    
 _ciidExclude_
  
> [in] Die Anzahl der Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden sollen.
    
 _rgiidExclude_
  
> [in] Ein Array von Schnittstellenbezeichnern, das Schnittstellen angibt, die nicht verwendet werden sollten, wenn Sie zusätzliche Informationen in das Zielobjekt kopieren oder verschieben.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftentags identifiziert, die vom Kopier- oder Verschiebungsvorgang ausgeschlossen werden sollen. Das Übergeben von NULL im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **DoCopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die von  _lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn NULL im  _lpProgress-Parameter_ übergeben wird, stellt MAPI die Implementierung des Fortschritts bereit. Der  _parameter lpProgress_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner, der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an. 
    
MAPI_MOVE 
  
> **DoCopyTo** sollte einen Verschiebungsvorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Kennzeichen nicht festgelegt ist, führt **DoCopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Kennzeichen nicht festgelegt ist, überschreibt **DoCopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine zu kopierende oder zu verschiebende Eigenschaft ist bereits im Zielobjekt vorhanden, und das flag MAPI_NOREPLACE festgelegt ist. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt enthält das Zielobjekt direkt oder indirekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise umfangreiche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird nicht von dem Objekt unterstützt, auf das von  _lpSrcObj_ verwiesen wird, oder die durch den  _lpDestInterface-Parameter_ identifizierte Schnittstelle wird von dem Objekt, auf das  _lpDestObj verweist,_ nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
MAPI_E_INVALID_PARAMETER 
  
> Der  _LpSrcInterface-Parameter_ ist NULL. 
    
Die folgenden Werte können in der **Struktur SPropProblemArray** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyTo**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **DoCopyTo** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp entspricht nicht dem Typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::D oCopyTo-Methode** ist für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **DoCopyTo** aufrufen, um die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) für ihre Ordner und Nachrichten zu implementieren. 
  
Standardmäßig kopiert oder verschiebt **DoCopyTo** alle Eigenschaften eines Objekts in ein anderes Objekt. Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und in ihrer Gesamtheit kopiert oder verschoben. 
  
Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE im  _ulFlags-Parameter_ festgelegt ist. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um Eigenschaften vom Kopier- oder Verschiebungsvorgang auszuschließen, schließen Sie deren Eigenschaftentags in den  _Parameter lpExcludeProps_ ein. Wenn Sie die Ergebnisse der Verwendung des [makros PROP_TAG](prop_tag.md) übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Beispielsweise bewirkt der folgende Eintrag im Eigenschaftentagarray, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im Eigenschaftstag-Ausschlussarray an. Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie die **Eigenschaft PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) zum Ausschlussarray hinzu. Um die Anlagen einer Nachricht auszuschließen, fügen Sie dem Array die **Eigenschaft PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) hinzu.
  
Um das Kopieren oder Verschieben der Hierarchie oder des Inhaltsverzeichnisses eines Ordners oder Adressbuchcontainers zu verhindern, schließen Sie **auch PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftstag-Ausschlussarray ein.
  
Ignorieren Sie MAPI_E_COMPUTED Fehler, die in der **Struktur "SPropProblemArray"** im  _Parameter "lppProblems"_ zurückgegeben werden. 
  
Der Schnittstellenbezeichner, auf den  _lpSrcInterface_ zeigt, ist in der Regel identisch mit dem Schnittstellenbezeichner, auf den  _lpDestInterface_ zeigt. 
  
Wenn Sie einen akzeptablen Schnittstellenbezeichner in  _lpDestInterface,_ aber einen ungültigen Zeiger in  _lpDestObj_ übergeben, sind die Ergebnisse unvorhersehbar. Dies führt wahrscheinlich dazu, dass Ihr Anbieter fehlschlägt. 
  
Wenn Sie dagegen ergänzende Informationen kennen, die nicht kopiert oder verschoben werden sollen, fügen Sie die Schnittstellenbezeichner für die Schnittstellen hinzu, die in dem array ausgeschlossen werden sollen, das im  _rgiidExclude-Parameter_ übergeben wird. Wenn Sie z. B. Nachrichten kopieren, aber keine ihrer Nachrichtenanlagen, übergeben Sie IID_IMessage im _rgiidExclude-Array._ **DoCopyTo** ignoriert alle in  _rgiidExclude_ aufgeführten Schnittstellen, die nicht erkannt werden. 
  
Wenn Sie den  _Parameter "rgiidExclude"_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Wenn Sie beispielsweise die [IMAPIContainer-Schnittstelle](imapicontainerimapiprop.md) ausschließen, werden Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen. Schließen Sie [IMAPIProp](imapipropiunknown.md) oder [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) nicht aus, da so viele Schnittstellen von ihnen abgeleitet sind. 
  
 **DoCopyTo** meldet globale Fehler, die für den gesamten Vorgang gelten, sowie einzelne Fehler, die für einzelne Eigenschaften gelten. Diese einzelnen Fehler werden in eine **SPropProblemArray-Struktur** eingefügt. Sie können die Fehlerberichterstattung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Arraystrukturparameter des Eigenschaftsproblems übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _Parameter "lppProblems"._ Wenn **DoCopyTo** S_OK zurückgibt, überprüfen Sie mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyTo** einen Fehler zurückgibt, werden in der **SPropProblemArray-Struktur** keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DoCopyTo** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn beim **DoCopyTo-Aufruf** ein globaler Fehler auftritt, verwenden oder geben Sie die **SPropProblemArray-Struktur** nicht frei. Anbieter sollten das  _ulIndex-Element_ in **SPropProblemArray-Strukturen** ignorieren, die von **DoCopyTo** zurückgegeben werden.
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[PidTagMessageAttachments (kanonische Eigenschaft)](pidtagmessageattachments-canonical-property.md)
  
[PidTagMessageDeliveryTime (kanonische Eigenschaft)](pidtagmessagedeliverytime-canonical-property.md)
  
[PidTagMessageRecipients (kanonische Eigenschaft)](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

