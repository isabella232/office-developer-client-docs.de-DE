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
ms.openlocfilehash: 5ce5aa8c43e284b493a0709808a196c6c6889f88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592108"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme von speziell Ausgeschlossene Eigenschaften in ein anderes Objekt.
  
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
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um das Objekt zuzugreifen, die über die Eigenschaften, kopiert oder verschoben werden soll.
    
 _lpSrcObj_
  
> [in] Ein Zeiger auf das Objekt, das die Eigenschaften kopiert oder verschoben werden.
    
 _ciidExclude_
  
> [in] Die Anzahl der Schnittstellen zum ausschließen, wenn Sie kopieren oder verschieben Sie Eigenschaften.
    
 _rgiidExclude_
  
> [in] Ein Array mit den IDs der Schnittstelle, Schnittstellen angibt, die beim Kopieren oder verschieben zusätzliche Informationen zum Zielobjekt nicht verwendet werden soll.
    
 _lpExcludeProps_
  
> [in] Ein Zeiger auf einen Tag Array-Eigenschaft, die die Eigenschaftentags identifiziert, die von der Kopie ausgeschlossen werden soll oder verschoben wird. Übergeben von NULL in der _LpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden soll. **DoCopyTo** zurückgegeben, dass MAPI_E_INVALID_PARAMETER, wenn das **cValues** Mitglied der [SPropTagArray](sproptagarray.md) -Struktur mit _LpExcludeProps_ gezeigt auf 0 gesetzt ist. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige. 
    
 _lpProgress_
  
> [in] Ein Zeiger auf eine Implementierung der Fortschritt-Symbol. Wenn NULL in der _LpProgress_ -Parameter übergeben wird, wird die Implementierung des Fortschritts von MAPI bereitgestellt. Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpDestInterface_
  
> [in] Ein Zeiger auf die Schnittstellenbezeichner, der die Schnittstelle für das Objekt, um die kopierte oder verschobenen Eigenschaften erhalten Zugriff auf verwendet werden darstellt.
    
 _lpDestObj_
  
> [in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Eine Statusanzeige angezeigt. 
    
MAPI_MOVE 
  
> **DoCopyTo** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt. Wenn dieses Flag nicht festgelegt ist, führt **DoCopyTo** durch einen Kopiervorgang. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyTo** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, gibt keine Notwendigkeit zur Fehlerinformationen an. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **DoCopyTo** ausführliche Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaften haben erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine Eigenschaft, die kopiert oder verschoben bereits vorhanden ist, im Zielobjekt, und das Flag MAPI_NOREPLACE festgelegt ist. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt enthält direkt oder indirekt Zielobjekt. Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die Schnittstelle, die vom _LpSrcInterface_ -Parameter wird nicht unterstützt, durch das Objekt, auf das _LpSrcObj_oder die Schnittstelle, die vom _LpDestInterface_ -Parameter wird durch das auf den _LpDestObj-Objekt nicht unterstützt _. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.
    
MAPI_E_INVALID_PARAMETER 
  
> Der Parameter _LpSrcInterface_ ist NULL. 
    
Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **DoCopyTo**zurückgegeben werden soll. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und **DoCopyTo** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **DoCopyTo** nur Unicode unterstützt. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht vom Anrufer erwartet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::DoCopyTo** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert. Nachricht Anbieter können **DoCopyTo** zum Implementieren der [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode für ihre Ordner und Nachrichten aufrufen. 
  
In der Standardeinstellung **DoCopyTo** kopiert oder verschiebt alle Eigenschaften eines Objekts in ein anderes Objekt. Alle Unterobjekte im Quellobjekt werden vollständig automatisch bei der Konflikte enthalten und kopiert oder verschoben. 
  
Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist. Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ausschließen von Eigenschaften aus der Kopie oder Verschiebevorgang, deren Eigenschaftentags im _LpExcludeProps_ -Parameter enthalten. Wenn Sie die Ergebnisse der Verwendung von Makros [PROP_TAG](prop_tag.md) zum Erstellen einer Eigenschaftentag aus einem bestimmten Kennzeichen im Array Tag-Eigenschaft übergeben wird, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen. Der folgende Eintrag im Array Tag-Eigenschaft bewirkt beispielsweise alle Eigenschaften mit der ID 0x8002, ausgeschlossen werden sollen, unabhängig vom Typ: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Geben Sie zum Vermeiden von Zeitaufwands für die Bereitstellung einer Nachricht, wenn Sie die Nachricht auf einen anderen Ordner kopieren, kopieren **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) die Array-Eigenschaft Tag ausschließen. Um eine Nachricht Empfängerliste auszuschließen, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft dem Exclude-Array. Um eine e-Mail-Anlagen auszuschließen, fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft dem Array hinzu.
  
Auf ähnliche Weise, um das Kopieren oder Verschieben eines Ordners oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu verhindern, schließen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in der Eigenschaft Tag Array ausschließen.
  
Ignorieren Sie MAPI_E_COMPUTED Fehler in der Struktur **SPropProblemArray** im _LppProblems_ -Parameter zurückgegeben. 
  
Der Schnittstellenbezeichner, die _LpSrcInterface_ verweist, ist in der Regel identisch mit der Identifier, _LpDestInterface_ verweist. 
  
Wenn Sie einen Schnittstellenbezeichner akzeptable in _LpDestInterface_ , aber ein ungültiger Zeiger in _LpDestObj_übergeben, sind die Ergebnisse unvorhersehbar. In den meisten Fällen bewirkt dies vom Dienstanbieter ein Fehler auftritt. 
  
Umgekehrt, wenn Sie zusätzliche Informationen, die nicht kopiert oder verschoben werden soll kennen, fügen Sie die als Schnittstellenbezeichner für die Schnittstellen, die in der _RgiidExclude_ -Parameter übergebenen Arrays ausgeschlossen werden hinzu. Wenn Sie Nachrichten, aber keine ihrer e-Mail-Anlagen kopieren, übergeben Sie IID_IMessage im Array _RgiidExclude_ fest. **DoCopyTo** ignoriert Schnittstellen, die in _RgiidExclude_ , die es nicht erkennt aufgelistet. 
  
Wenn Sie den Parameter _RgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle Schnittstellen, die von dieser Schnittstelle abgeleitet ausgeschlossen. Die Schnittstelle [IMAPIContainer](imapicontainerimapiprop.md) ausschließen bewirkt beispielsweise, dass Ordner oder Adresse Adressbuch-Container, je nach den Typ des Anbieters ausgeschlossen werden sollen. Schließen Sie keine [IMAPIProp](imapipropiunknown.md) oder [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , da so viele Schnittstellen, die von ihnen abgeleitet werden. 
  
 **DoCopyTo** meldet globale Fehlern, die für den Vorgang als Ganzes gelten und einzelnen Fehler, die für die einzelnen Eigenschaften gelten. Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt. Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie NULL, statt dass ein gültiger Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters. Wenn **DoCopyTo** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyTo** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben. Rufen Sie stattdessen die [IMAPISupport::GetLastError](imapisupport-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen. 
  
Wenn **DoCopyTo** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
Wenn bei der **DoCopyTo** Aufruf ein globaler Fehler auftritt, nicht verwenden oder die Struktur **SPropProblemArray** frei. Anbieter sollte das _UlIndex_ -Element in **SPropProblemArray** Strukturen zurückgegebene **DoCopyTo**ignoriert werden.
  
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

