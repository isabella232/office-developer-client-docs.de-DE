---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6d65a0103e86b89aa051c41a1597d0b2208aa33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596141"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Eintragsbezeichner für eine einmalige Adresse.
  
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
  
> [in] Ein Zeiger auf den Anzeigenamen des Empfängers der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft. Der  _lpszName-Parameter_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp (z. B. FAX, SMTP oder X500) des Empfängers. Der  _LpszAdrType-Parameter_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die Messagingadresse des Empfängers. Der  _Parameter lpszAddress_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt. Die folgenden Flags können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierte Nachrichteninhalte nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) des Empfängers auf FALSE fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messagingadresse des Empfängers, auf die von  _lpszAddress_ verwiesen wird, wird als Internetadresse interpretiert. In diesem Fall legt MAPI **PR_SEND_RICH_INFO** auf FALSE fest. 
    
MAPI_UNICODE 
  
> Der Anzeigename, der Adresstyp und die Adresse haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben diese Zeichenfolgen das ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Anzahl der Bytes im Eintragsbezeichner, auf den der  _Parameter "lppEntryID"_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner für den einmaligen Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::CreateOneOff-Methode** wird für alle Supportobjekte des Dienstanbieters implementiert. Dienstanbieter rufen **CreateOneOff** auf, um einen Eintragsbezeichner für einen einmaligen Empfänger (einen Empfänger, der keinem der Container von einem der aktuell geladenen Adressbuchanbieter angehört) zu erstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie mit der Verwendung des von **CreateOneOff** zurückgegebenen Eintragsbezeichners fertig sind, geben Sie den für den Eintragsbezeichner reservierten Speicher mithilfe der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei. 
  
## <a name="notes-to-transport-providers"></a>Hinweise zu Transportanbietern

Unterstützen Sie das Transport Neutral Encapsulation Format (TNEF), und verwenden Sie den Wert der **PR_SEND_RICH_INFO-Eigenschaft,** um zu bestimmen, ob TNEF beim Transport einer Nachricht verwendet werden soll. Das Nicht-Unterstützen von TNEF oder das Senden einer Nachricht in diesem Format, wenn sie angefordert wird, kann für formularbasierte Clients oder Clients, die benutzerdefinierte MAPI-Eigenschaften erfordern, ein Problem darstellen. Dies liegt daran, dass TNEF in der Regel verwendet wird, um benutzerdefinierte Eigenschaften für benutzerdefinierte Nachrichtenklassen zu senden. 
  
## <a name="see-also"></a>Siehe auch



[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagDisplayName (kanonische Eigenschaft)](pidtagdisplayname-canonical-property.md)
  
[PidTagSendRichInfo (kanonische Eigenschaft)](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

