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
  
Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme der explizit ausgeschlossenen Eigenschaften, in ein anderes Objekt.
  
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
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, das über die Eigenschaften verfügt, die kopiert oder verschoben werden sollen.
    
 _lpSrcObj_
  
> in Ein Zeiger auf das Objekt, das die Eigenschaften enthält, die kopiert oder verschoben werden sollen.
    
 _ciidExclude_
  
> in Die Anzahl von Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden sollen.
    
 _rgiidExclude_
  
> in Ein Array von Schnittstellen Bezeichnern, das Schnittstellen angibt, die beim Kopieren oder verschieben zusätzlicher Informationen in das Zielobjekt nicht verwendet werden sollen.
    
 _lpExcludeProps_
  
> in Ein Zeiger auf ein Property-Tag-Array, das die Eigenschaftentags identifiziert, die vom Kopier-oder Verschiebungsvorgang ausgeschlossen werden sollen. Das übergeben von NULL im _lpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen. **DoCopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues** -Element der [SPropTagArray](sproptagarray.md) -Struktur, auf die durch _lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> in Ein Zeiger auf eine Statusindikator-Implementierung. Wenn NULL im _lpProgress_ -Parameter übergeben wird, stellt MAPI die Status Implementierung bereit. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpDestInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner, der die Schnittstelle darstellt, die für den Zugriff auf das Objekt zum Abrufen der kopierten oder verschobenen Eigenschaften verwendet werden soll.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an. 
    
MAPI_MOVE 
  
> **DoCopyTo** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen. Wenn dieses Flag nicht festgelegt ist, führt **DoCopyTo** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> Out Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **DoCopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine Eigenschaft, die kopiert oder verschoben werden soll, ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE-Flag wird festgelegt. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpSrcInterface_ -Parameter angegebene Schnittstelle wird von dem Objekt, auf das durch _lpSrcObj_verwiesen wird, nicht unterstützt, oder die durch den _lpDestInterface_ -Parameter angegebene Schnittstelle wird von dem Objekt, auf das durch _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
MAPI_E_INVALID_PARAMETER 
  
> Der _lpSrcInterface_ -Parameter ist NULL. 
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyTo**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **DoCopyTo** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyTo** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D ocopyto** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter können **DoCopyTo** aufrufen, um die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode für Ihre Ordner und Nachrichten zu implementieren. 
  
Standardmäßig kopiert **DoCopyTo** alle Eigenschaften eines Objekts in ein anderes Objekt. Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang eingeschlossen und vollständig kopiert oder verschoben. 
  
Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleiben unberührt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um Eigenschaften aus dem Kopier-oder Verschiebungsvorgang auszuschließen, schließen Sie deren Eigenschaftstags in den Parameter _lpExcludeProps_ ein. Wenn Sie die Ergebnisse der Verwendung des [PROP_TAG](prop_tag.md) -Makros zum Erstellen eines Eigenschaftentags aus einem bestimmten Bezeichner im Property-Tag-Array überschreiten, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Beispielsweise bewirkt der folgende Eintrag im Property Tag-Array, dass alle Eigenschaften mit einem Bezeichner von 0x8002 unabhängig vom Typ ausgeschlossen werden: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Um zu verhindern, dass die Übermittlungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md)) im Property-Tag Exclude-Array an. Wenn Sie die Empfängerliste einer Nachricht ausschließen möchten, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft zum Exclude-Array hinzu. Zum Ausschließen der Anlagen einer Nachricht fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft zum Array hinzu.
  
Um zu verhindern, dass ein Ordner-oder Adressbuchcontainer die Hierarchie-oder Inhaltstabelle kopiert oder verschiebt, schließen Sie **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) im Property-Tag Exclude-Array.
  
Ignoriert MAPI_E_COMPUTED-Fehler, die in der **SPropProblemArray** -Struktur im _lppProblems_ -Parameter zurückgegeben werden. 
  
Der Schnittstellenbezeichner, auf den _lpSrcInterface_ verweist, ist in der Regel derselbe wie der Schnittstellenbezeichner, auf den _lpDestInterface_ verweist. 
  
Wenn Sie einen akzeptablen Schnittstellenbezeichner in _lpDestInterface_ , jedoch einen ungültigen Zeiger in _lpDestObj_, sind die Ergebnisse unvorhersehbar. Dies führt zu einem Fehler des Anbieters. 
  
Wenn Sie jedoch zusätzliche Informationen kennen, die nicht kopiert oder verschoben werden sollen, fügen Sie die Schnittstellenbezeichner für die Schnittstellen hinzu, die in dem im _rgiidExclude_ -Parameter übergebenen Array ausgeschlossen werden sollen. Wenn Sie beispielsweise Nachrichten kopieren, jedoch keine Ihrer Nachrichtenanlagen, führen Sie IID_IMessage im _rgiidExclude_ -Array aus. **DoCopyTo** ignoriert alle in _rgiidExclude_ aufgeführten Schnittstellen, die nicht erkannt werden. 
  
Wenn Sie den Parameter _rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen. Wenn Sie beispielsweise die [IMAPIContainer](imapicontainerimapiprop.md) -Schnittstelle ausschließen, werden Ordner oder Adressbuchcontainer abhängig vom Anbietertyp ausgeschlossen. Schließen Sie [IMAPIProp](imapipropiunknown.md) oder [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) nicht aus, da so viele Schnittstellen von Ihnen abgeleitet werden. 
  
 **DoCopyTo** meldet globale Fehler, die für den Vorgang als Ganzes gelten, sowie einzelne Fehler, die für einzelne Eigenschaften gelten. Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt. Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschaft "NULL" übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **DOCOPYTO** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyTo** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPISupport:: getlasterroraufzurufen](imapisupport-getlasterror.md) -Methode auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DOCOPYTO** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
Wenn ein globaler Fehler beim **DoCopyTo** -Aufruf auftritt, verwenden oder befreien Sie die **SPropProblemArray** -Struktur nicht. Anbieter sollten das _ulIndex_ -Element in **SPropProblemArray** -Strukturen, die von **DoCopyTo**zurückgegeben werden, ignorieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Kanonische Pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische Pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische Pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische Pidtagmessagedeliverytime (-Eigenschaft](pidtagmessagedeliverytime-canonical-property.md)
  
[Kanonische Pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

