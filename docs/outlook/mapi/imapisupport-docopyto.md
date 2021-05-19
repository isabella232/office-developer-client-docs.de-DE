---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331808"
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
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, das über die Eigenschaften verfügt, die kopiert oder verschoben werden sollen.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das die eigenschaften enthält, die kopiert oder verschoben werden sollen.
    
 _ciidExclude_
  
> [in] Die Anzahl der Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden.
    
 _rgiidExclude_
  
> [in] Ein Array von Schnittstellenbezeichnern, das Schnittstellen angibt, die nicht verwendet werden sollten, wenn Sie ergänzende Informationen kopieren oder in das Zielobjekt verschieben.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftstags identifiziert, die vom Kopier- oder Verschiebevorgang ausgeschlossen werden sollen. Das Übergeben von NULL im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **DoCopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn **das cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die  _von lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Fortschrittsindikatorimplementierung. Wenn NULL im  _lpProgress-Parameter übergeben_ wird, stellt MAPI die Fortschrittsimplementierung. Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID, die die Schnittstelle darstellt, mit der auf das Objekt zugegriffen werden soll, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an. 
    
MAPI_MOVE 
  
> **DoCopyTo** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen. Wenn dieses Flag nicht festgelegt ist, **führt DoCopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Kennzeichen nicht festgelegt ist, **überschreibt DoCopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine zu kopierende oder zu verschobene Eigenschaft ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE ist festgelegt. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Quellobjekt enthält direkt oder indirekt das Zielobjekt. Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die durch den  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird vom objekt, auf das  _von lpSrcObj_ verwiesen wird, nicht unterstützt, oder die durch den  _lpDestInterface-Parameter_ identifizierte Schnittstelle wird vom Objekt, auf das von  _lpDestObj_ verwiesen wird, nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
MAPI_E_INVALID_PARAMETER 
  
> Der  _lpSrcInterface-Parameter_ ist NULL. 
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyTo**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE festgelegt, und **DoCopyTo** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, und **DoCopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der typ, der vom Aufrufer erwartet wird.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::D oCopyTo-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter können **DoCopyTo aufrufen,** um die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) für ihre Ordner und Nachrichten zu implementieren. 
  
Standardmäßig kopiert oder verschiebt **DoCopyTo** alle Eigenschaften eines Objekts in ein anderes Objekt. Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben. 
  
Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE wird im  _ulFlags-Parameter_ festgelegt. Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um Eigenschaften aus dem Kopier- oder Verschiebevorgang auszuschließen, schließen Sie ihre Eigenschaftstags in den  _lpExcludeProps-Parameter_ ein. Wenn Sie die Ergebnisse [](prop_tag.md) der Verwendung des PROP_TAG-Makros übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Der folgende Eintrag im Eigenschaftentagarray bewirkt beispielsweise, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im #A0 aus. Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie **die PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft zum Exclude-Array hinzu. Zum Ausschließen der Anlagen einer Nachricht fügen Sie **die PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft zum Array hinzu.
  
Um das Kopieren oder Verschieben der Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers zu verhindern, schließen Sie **auch PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das #A0 ein.
  
Ignorieren MAPI_E_COMPUTED Fehler, die in der **SPropProblemArray-Struktur** im  _lppProblems-Parameter zurückgegeben_ werden. 
  
Der Schnittstellenbezeichner, auf den  _lpSrcInterface_ verweist, ist in der Regel identisch mit dem Schnittstellenbezeichner, auf den  _lpDestInterface_ verweist. 
  
Wenn Sie einen akzeptablen Schnittstellenbezeichner in  _lpDestInterface,_ aber einen ungültigen Zeiger in  _lpDestObj_ übergeben, sind die Ergebnisse unvorhersehbar. Dies wird höchstwahrscheinlich dazu führen, dass Ihr Anbieter fehlschlägt. 
  
Wenn Ihnen hingegen ergänzende Informationen bekannt sind, die nicht kopiert oder verschoben werden sollten, fügen Sie die Schnittstellenbezeichner für die Schnittstellen hinzu, die im Array ausgeschlossen werden sollen, das im  _rgiidExclude-Parameter_ übergeben wird. Wenn Sie z. B. Nachrichten kopieren, aber keine ihrer Nachrichtenanlagen, übergeben Sie IID_IMessage im _rgiidExclude-Array._ **DoCopyTo** ignoriert alle in  _rgiidExclude_ aufgeführten Schnittstellen, die nicht erkannt werden. 
  
Wenn Sie den  _Parameter rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Wenn Sie beispielsweise die [IMAPIContainer-Schnittstelle](imapicontainerimapiprop.md) ausschließen, werden Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen. Schließen Sie [IMAPIProp](imapipropiunknown.md) oder [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) nicht aus, da so viele Schnittstellen von ihnen stammen. 
  
 **DoCopyTo** meldet globale Fehler, die für den gesamten Vorgang gelten, und einzelne Fehler, die für einzelne Eigenschaften gelten. Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** angezeigt. Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Parameter für die Arraystruktur des Eigenschaftsproblems übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._ Wenn **DoCopyTo** S_OK, suchen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyTo** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DoCopyTo** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen. 
  
Wenn beim **DoCopyTo-Aufruf** ein globaler Fehler auftritt, verwenden oder geben Sie die **SPropProblemArray-Struktur nicht** frei. Anbieter sollten das _ulIndex-Element_ in den von **DoCopyTo** zurückgegebenen **SPropProblemArray-Strukturen** ignorieren.
  
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

