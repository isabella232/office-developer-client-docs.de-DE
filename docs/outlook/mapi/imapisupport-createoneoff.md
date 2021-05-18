---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411995"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Eintragsbezeichner für eine eindeutige Adresse.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpszName_
  
> [in] Ein Zeiger auf den Anzeigenamen des Empfängers, **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft. Der  _lpszName-Parameter_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp (z. B. FAX, SMTP oder X500) des Empfängers. Der  _lpszAdrType-Parameter_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die Messagingadresse des Empfängers. Der  _lpszAddress-Parameter_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die sich auf den einmalen Empfänger auswirkt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierte Nachrichteninhalte nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **Eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) des Empfängers auf FALSE fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die von  _lpszAddress_ angezeigte Messagingadresse des Empfängers wird als Internetadresse interpretiert. In diesem Fall legt MAPI **PR_SEND_RICH_INFO** FALSE fest. 
    
MAPI_UNICODE 
  
> Anzeigename, Adresstyp und Adresse befinden sich im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Anzahl der Bytes in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmal verwendeten Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der eindeutige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::CreateOneOff-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **CreateOneOff auf,** um eine Eintrags-ID für einen einzigen Empfänger (einen Empfänger, der keinem der Container von einem der derzeit geladenen Adressbuchanbieter angehört) zu erstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie mit der von **CreateOneOff** zurückgegebenen Eintrags-ID fertig sind, wird der für die Eintrags-ID zugewiesene Arbeitsspeicher mithilfe der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei. 
  
## <a name="notes-to-transport-providers"></a>Hinweise zu Transportanbietern

Unterstützen Sie das Transport Neutral Encapsulation Format (TNEF) und verwenden Sie den Wert der **PR_SEND_RICH_INFO-Eigenschaft,** um zu bestimmen, ob TNEF beim Transport einer Nachricht verwendet werden soll. Die Nicht-Unterstützung von TNEF oder das Senden einer Nachricht in diesem Format, wenn sie angefordert wird, kann ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften benötigen. Dies liegt daran, dass TNEF in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagDisplayName (kanonische Eigenschaft)](pidtagdisplayname-canonical-property.md)
  
[PidTagSendRichInfo (kanonische Eigenschaft)](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

