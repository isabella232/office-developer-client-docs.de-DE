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
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349287"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie die Inhaltstabelle zurückgegeben wird. Die folgenden Flags können festgelegt werden:
    
MAPI_ASSOCIATED 
  
> Die Tabelle mit den zugeordneten Inhalten des Containers sollte anstelle der Standardinhalts Tabelle zurückgegeben werden. Dieses Flag wird nur mit Ordnern verwendet. Die Nachrichten, die in der Tabelle zugeordnete Inhalte enthalten sind, wurden mit dem MAPI_ASSOCIATED-Flag erstellt, das im Aufruf der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode festgelegt wurde. Clients verwenden in der Regel die zugeordnete Inhaltstabelle, um Formulare, Ansichten und andere ausgeblendete Nachrichten abzurufen. 
    
ACLTABLE_FREEBUSY
  
> Ermöglicht den Zugriff auf die frightsFreeBusySimple-und frightsFreeBusyDetailed-Rechte in **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **** Getcontentable kann erfolgreich zurückgegeben werden, bevor die Tabelle dem Aufrufer zur Verfügung gestellt wird. Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellen Aufruf ein Fehler ausgelöst werden. 
    
MAPI_UNICODE 
  
> Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als weich gelöscht markiert sind, d. h., Sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Inhaltstabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Inhaltstabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container hat keinen Inhalt und kann keine Inhaltstabelle bereitstellen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer::** getcontentable-Methode gibt einen Zeiger auf die Inhaltstabelle eines Containers zurück. Eine Inhaltstabelle enthält zusammenfassende Informationen zu Objekten im Container. 
  
Inhaltstabellen haben lange Spaltensätze. Eine vollständige Liste der erforderlichen und optionalen Spalten in Inhaltstabellen finden Sie unter [Inhaltstabellen](contents-tables.md). 
  
Es ist möglich, dass einige Container keinen Inhalt haben. Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen **** von getcontentable zurück.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie eine Inhaltstabelle für ihren Container unterstützen, müssen Sie auch Folgendes tun:
  
- Unterstützen Sie Aufrufe der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers, um die **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))-Eigenschaft zu öffnen.
    
- Zurückgeben von **PR_CONTAINER_CONTENTS** als Reaktion auf einen Aufruf des Containers 
    
    [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methoden. 
    
Die Implementierung dieser Methode durch einen Remote Transportanbieter muss einen Zeiger auf eine [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle im _ppTable_ -Parameter zurückgeben, der an die getcontentable-Methode übergeben wird. **** Wenn Ihr Transportanbieter über eine vorhandene Inhaltstabelle verfügt, genügt es, einen Zeiger darauf zurückzugeben. Wenn dies nicht der Fall ist, muss diese Methode ein neues [IMAPITable: IUnknown](imapitableiunknown.md) -Objekt erstellen, die Tabelle mit Nachrichtenheadern Auffüllen (sofern vorhanden), und einen Zeiger auf die neue Tabelle zurückgeben. Die [ITableData:: HrGetView](itabledata-hrgetview.md) -Methode ist nützlich, um einen Rückgabewert zu generieren und den Tabellen Zeiger im _ppTable_ -Parameter zu speichern. Die Contents-Tabelle muss mindestens die folgenden Eigenschaftsspalten unterstützen: 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([Pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([Pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([Pidtaghasattachments (](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Tabellenspalten für String-und Binary-Inhalte können abgeschnitten werden. In der Regel geben Anbieter 255 Zeichen zurück. Da Sie nicht vorher wissen können, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 255 oder 510 Byte beträgt. Sie können den vollständigen Wert einer abgeschnittenen Spalte, falls erforderlich, jederzeit direkt aus dem Objekt abrufen, indem Sie die Eintrags-ID verwenden, um Sie zu öffnen und dann die **IMAPIProp::** GetProps-Methode aufzurufen. 
  
Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge für alle Zeichenfolgen oder die gekürzte Version dieser Zeichenfolge gelten.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableDialog. cpp  <br/> |CContentsTableDlg:: CContentsTableDlg  <br/> |Die **CContentsTableDlg** -Klasse **** verwendet getcontentable, um die Einträge in einer Inhaltstabelle abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Kanonische Pidtagcontainercontents (-Eigenschaft](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

