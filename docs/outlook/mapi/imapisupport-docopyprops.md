---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322365"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert oder verschiebt eine oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
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
  
> in Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt mit den Eigenschaften verwendet werden soll, die kopiert oder verschoben werden sollen.
    
 _lpSrcObj_
  
> in Ein Zeiger auf das Objekt, das die Eigenschaften enthält, die kopiert oder verschoben werden sollen.
    
 _lpIncludeProps_
  
> in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Gezähltes Array von Property-Tags enthält, die die zu kopierende oder zu verschiebende Eigenschaft kennzeichnet. Der _lpIncludeProps_ -Parameter darf nicht NULL sein. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _lpProgress_
  
> in Ein Zeiger auf eine Implementierung einer Statusanzeige. Wenn NULL im _lpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt. Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpDestInterface_
  
> in Ein Zeiger auf den Schnittstellenbezeichner, der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, um die Eigenschaften zu empfangen, die kopiert oder verschoben werden.
    
 _lpDestObj_
  
> in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie der Kopier-oder Verschiebungsvorgang ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Statusanzeige an.
    
MAPI_MOVE 
  
> **DoCopyProps** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen. Wenn dieses Flag nicht festgelegt ist, führt **DoCopyProps** einen Kopiervorgang aus. 
    
MAPI_NOREPLACE 
  
> Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden. Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyProps** vorhandene Eigenschaften. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **DoCopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Eigenschaften wurden erfolgreich kopiert oder verschoben.
    
MAPI_E_COLLISION 
  
> Eine Eigenschaft, die kopiert oder verschoben werden soll, ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE-Flag wird festgelegt. 
    
MAPI_E_FOLDER_CYCLE 
  
> Das Source-Objekt enthält direkt oder indirekt das Zielobjekt. Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die vom _lpSrcInterface_ -Parameter angegebene Schnittstelle wird vom Source-Objekt nicht unterstützt, oder die vom _lpDestInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt. 
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt. Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyProps**. Diese Fehler gelten für eine einzelne Eigenschaft.
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **DoCopyProps** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyProps** unterstützt nur Unicode. 
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird. Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D ocopyprops** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter können **DoCopyProps** aufrufen, um die [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Methode für Ihre Ordner und Nachrichten zu implementieren. **DoCopyProps** kopiert oder verschiebt die Eigenschaften, die im Eigenschaftentag-Array identifiziert werden, auf das von _lpIncludeProps_ verwiesen wird, und die in dem Objekt vorhanden sind, auf das durch _lpSrcObj_verwiesen wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie Eigenschaften zwischen Objekten desselben Typs kopieren, beispielsweise zwei Nachrichten, müssen die Parameter _lpSrcInterface_ und _lpDestInterface_ den gleichen Schnittstellenbezeichner und die Parameter _lpSrcObj_ und _lpDestObj_ enthalten. muss auf Objekte desselben Typs zeigen. Wenn _lpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER zurück. Wenn Sie _lpDestInterface_ auf einen akzeptablen Schnittstellenbezeichner festlegen, aber _lpDestObj_ auf einen ungültigen Zeiger festlegen, sind die Ergebnisse unvorhersehbar. Wahrscheinlich schlägt Ihr Anbieter fehl. 
  
Legen Sie das MAPI_NOREPLACE-Flag fest, wenn keine der Eigenschaften im Zielobjekt überschrieben werden soll. Eigenschaften im Zielobjekt, die im Quellobjekt vorhanden sind und nicht überschrieben werden, werden nicht gelöscht oder geändert.
  
Um die Empfängerliste einer Nachricht zu kopieren, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft in das Tag-Array der Eigenschaft ein, auf die durch den _lpIncludeProps_ -Parameter verwiesen wird. Schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft ein, um die Anlagen der Nachricht zu kopieren. 
  
Um eine Ordner-oder Adressbuchcontainer-Hierarchie-oder Inhaltstabelle zu kopieren, schließen Sie **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) im Property-Tag-Array ein. Schließen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in das Array ein, um die zugeordnete Inhaltstabelle eines Ordners einzuschließen.
  
Wenn Unterordner kopiert oder verschoben werden, werden Ihre Inhalte unabhängig von der Verwendung von Eigenschaften, die von der **SPropTagArray** -Struktur angegeben werden, vollständig kopiert oder verschoben. 
  
 **DoCopyProps** meldet globale Fehler, die mit dem Vorgang als Ganzes auftreten, sowie einzelne Fehler, die mit einer oder mehreren Eigenschaften auftreten. Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt. Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschaft "NULL" übergeben. 
  
Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter. Wenn **DOCOPYPROPS** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur. Wenn **DoCopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben. Rufen Sie stattdessen die [IMAPISupport:: getlasterroraufzurufen](imapisupport-getlasterror.md) -Methode auf, um detaillierte Fehlerinformationen abzurufen. 
  
Wenn **DOCOPYPROPS** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Kanonische Pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[Kanonische Pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[Kanonische Pidtagfolderassociatedcontents (-Eigenschaft](pidtagfolderassociatedcontents-canonical-property.md)
  
[Kanonische Pidtagmessageattachments (-Eigenschaft](pidtagmessageattachments-canonical-property.md)
  
[Kanonische Pidtagmessagerecipients (-Eigenschaft](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

