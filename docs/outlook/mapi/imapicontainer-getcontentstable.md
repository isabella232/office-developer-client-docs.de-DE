---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: adccaaf30fb2deaf97a6b469170e529fa7121750
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616803"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf das Inhaltsverzeichnis des Containers zurück.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Inhaltsverzeichnis zurückgegeben wird. Die folgenden Flags können festgelegt werden:
    
MAPI_ASSOCIATED 
  
> Das zugeordnete Inhaltsverzeichnis des Containers sollte anstelle des Standardinhaltsverzeichnisses zurückgegeben werden. Dieses Flag wird nur für Ordner verwendet. Die Nachrichten, die im zugeordneten Inhaltsverzeichnis enthalten sind, wurden mit dem MAPI_ASSOCIATED Flag erstellt, das im Aufruf der [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) festgelegt wurde. Clients verwenden in der Regel das zugeordnete Inhaltsverzeichnis, um Formulare, Ansichten und andere ausgeblendete Nachrichten abzurufen. 
    
ACLTABLE_FREEBUSY
  
> Ermöglicht den Zugriff auf die Rechte "frightsFreeBusySimple" und "frightsFreeBusyDetailed" in **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** kann erfolgreich zurückgegeben werden, möglicherweise bevor die Tabelle dem Aufrufer zur Verfügung gestellt wird. Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellenaufruf ein Fehler ausgelöst werden. 
    
MAPI_UNICODE 
  
> Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden. Wenn das flag MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als vorläufig gelöscht markiert sind, d. h., sie befinden sich in der Aufbewahrungszeitphase für gelöschte Elemente.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf das Inhaltsverzeichnis.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Inhaltsverzeichnis wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container hat keinen Inhalt und kann kein Inhaltsverzeichnis bereitstellen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer::GetContentsTable-Methode** gibt einen Zeiger auf das Inhaltsverzeichnis eines Containers zurück. Ein Inhaltsverzeichnis enthält zusammenfassende Informationen zu Objekten im Container. 
  
Inhaltstabellen verfügen über lange Spaltensätze. Eine vollständige Liste der erforderlichen und optionalen Spalten in Inhaltstabellen finden Sie unter [Inhaltstabellen.](contents-tables.md) 
  
Es ist möglich, dass einige Container keinen Inhalt haben. Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen von **GetContentsTable** zurück.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie ein Inhaltsverzeichnis für Ihren Container unterstützen, müssen Sie auch Folgendes tun:
  
- Unterstützen Sie Aufrufe der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers, um die **eigenschaft PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) zu öffnen.
    
- Zurückgeben **PR_CONTAINER_CONTENTS** als Reaktion auf einen Aufruf des Containers 
    
    [IMAPIProp::GetProps-](imapiprop-getprops.md) und [IMAPIProp::GetPropList-Methoden.](imapiprop-getproplist.md) 
    
Die Implementierung dieser Methode durch einen Remotetransportanbieter muss einen Zeiger auf eine [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) im  _ppTable-Parameter_ zurückgeben, der an die **GetContentsTable-Methode** übergeben wird. Wenn Ihr Transportanbieter über ein vorhandenes Inhaltsverzeichnis verfügt, reicht es aus, um einen Zeiger darauf zurückzugeben. Andernfalls muss diese Methode ein neues [IMAPITable -Objekt erstellen: IUnknown-Objekt,](imapitableiunknown.md) die Tabelle mit Nachrichtenkopfzeilen auffüllen (sofern vorhanden), und einen Zeiger auf die neue Tabelle zurückgeben. Die [ITableData::HrGetView-Methode](itabledata-hrgetview.md) ist nützlich, um einen Rückgabewert zu generieren und den Tabellenzeiger im  _PpTable-Parameter_ zu speichern. Das Inhaltsverzeichnis muss mindestens die folgenden Eigenschaftenspalten unterstützen: 
  
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

Tabellenspalten für Zeichenfolgen und binäre Inhalte können abgeschnitten werden. In der Regel geben Anbieter 255 Zeichen zurück. Da Sie im Voraus nicht wissen können, ob eine Tabelle abgeschnittene Spalten enthält, gehen Sie davon aus, dass eine Spalte abgeschnitten ist, wenn die Länge der Spalte 255 oder 510 Byte beträgt. Sie können den vollständigen Wert einer abgeschnittenen Spalte bei Bedarf direkt aus dem Objekt abrufen, indem Sie den Eintragsbezeichner zum Öffnen verwenden und dann die **IMAPIProp::GetProps-Methode** aufrufen. 
  
Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge auf alle Zeichenfolgen oder auf die gekürzte Version dieser Zeichenfolge angewendet werden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |Die **CContentsTableDlg-Klasse** verwendet **GetContentsTable,** um die Einträge in einem Inhaltsverzeichnis abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerContents (kanonische Eigenschaft)](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

