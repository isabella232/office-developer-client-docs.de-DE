---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792082"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Betrifft**: Outlook 
  
Gibt einen Zeiger auf den Container Inhaltstabelle.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Inhaltstabelle zurückgegeben werden. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_ASSOCIATED 
  
> Der Container zugeordneten Inhaltstabelle sollten anstelle der standard Inhaltstabelle zurückgegeben werden. Dieses Kennzeichen werden nur bei Ordnern verwendet. Die Nachrichten, die in der zugehörigen Inhaltstabelle enthalten sind wurden mit dem MAPI_ASSOCIATED-Flag festlegen im Aufruf der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode erstellt. Clients verwenden in der Regel die zugehörige Inhaltstabelle, um Formulare, Ansichten und anderen ausgeblendeten Nachrichten abzurufen. 
    
ACLTABLE_FREEBUSY
  
> Ermöglicht den Zugriff auf die Rechte FrightsFreeBusySimple und FrightsFreeBusyDetailed in **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** können erfolgreich, möglicherweise beendet, bevor die Tabelle mit dem Anrufer verfügbar gemacht wird. Wenn die Tabelle nicht verfügbar ist, kann die nachfolgenden Tabelle Anrufen ein Fehler ausgelöst. 
    
PARAMETER MAPI_UNICODE 
  
> Anforderungen, die die Spalten, die Zeichenfolgendaten enthält das Unicode-Format zurückgegeben werden soll. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Inhaltstabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Inhaltstabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container über keinen Inhalt verfügt und eine Inhaltstabelle nicht bereitstellen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer::GetContentsTable** -Methode gibt einen Zeiger auf die Inhaltstabelle eines Containers. Eine Inhaltstabelle enthält zusammenfassende Informationen zu Objekten im Container. 
  
Inhalt Tabellen haben langen Spalte festgelegt. Eine vollständige Liste der erforderlichen und optionalen Spalten in Tabellen Inhalt finden Sie unter [Inhalt Tabellen](contents-tables.md). 
  
Es ist möglich, dass einige Container keinen Inhalt haben. Diese Container zurück MAPI_E_NO_SUPPORT aus ihrer Implementierungen von **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie eine Inhaltstabelle für den Container unterstützen, müssen Sie auch Folgendes:
  
- Supportanrufe an den Container [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))-Eigenschaft.
    
- Zurückgeben von **PR_CONTAINER_CONTENTS** Reaktion auf einen Aufruf an des Containers 
    
    [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methoden. 
    
Eine remote Adressbuchhierarchie Implementierung dieser Methode muss einen Zeiger auf Zurückgeben einer [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle in der _PpTable_ -Parameter an **den Befehl GetContentsTable** übergeben. Wenn Ihre Adressbuchhierarchie eine vorhandenen Inhaltstabelle aufweist, ist es ausreichend, um einen Zeiger darauf zurück. Wenn nicht, diese Methode ein neues erstellen muss [IMAPITable: IUnknown](imapitableiunknown.md) -Objekts, füllen Sie die Tabelle mit Kopfzeilen (falls verfügbar) und ein Zeiger auf die neue Tabelle zurückgegeben. Die [ITableData::HrGetView](itabledata-hrgetview.md) -Methode eignet sich für ein Rückgabewert generieren und Speichern von der Tabelle Zeiger in der _PpTable_ -Parameter. Die Inhaltstabelle muss mindestens die folgenden Spalten unterstützen: 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zeichenfolge und der binären Inhalt Tabellenspalten können abgeschnitten werden. In der Regel zurückgeben Anbieter 255 Zeichen. Da Sie im Voraus wissen können nicht, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen Sie, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 510 maximal 255 Bytes ist. Sie können immer den vollständigen Wert der abgeschnittene Spalte an, falls erforderlich, direkt aus dem Objekt mithilfe der Eintrags-ID um zu öffnen und anschließendes Aufrufen der **IMAPIProp::GetProps** -Methode abrufen. 
  
Je nach der Implementierung des Anbieters, Einschränkungen und Sortierung Vorgänge können auf alle einer Zeichenfolge oder auf die abgeschnittene Version dieser Zeichenfolge anwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |Die **CContentsTableDlg** -Klasse verwendet **GetContentsTable** , um die Einträge in einer Inhaltstabelle abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

