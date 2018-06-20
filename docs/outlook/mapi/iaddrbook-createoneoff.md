---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791998"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Betrifft**: Outlook 
  
Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.
  
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

 _Wert_
  
> [in] Ein Zeiger auf den Wert des Empfängers **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft. Der _Wert_ -Parameter kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Typ des Empfängers, wie FAX oder SMTP-Adresse. Der Parameter _LpszAdrType_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die Adresse des Empfängers. Der Parameter _LpszAddress_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den einmal-Empfänger auswirkt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann nicht formatierte Nachrichteninhalt behandeln. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, wird der MAPI-Eigenschaft des Empfängers- **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) auf false festgelegt. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, wird diese Eigenschaft von MAPI auf TRUE festgelegt, es sei denn, die Adresse des Empfängers messaging auf das _LpszAddress_ interpretiert wird, um eine IP-Adresse sein. In diesem Fall wird MAPI **PR_SEND_RICH_INFO** auf false festgelegt. 
    
PARAMETER MAPI_UNICODE 
  
> Der Anzeigename, Adresstyp und Adresse sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen in ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppEntryID_ verwiesen. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bezeichner des Eingangs wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Clients rufen die **CreateOneOff** -Methode zum Erstellen eines Eintrags-ID für einen einmaligen Empfänger – einen Empfänger, die nicht zu keiner der Container aus der aktuell geladenen adressbuchanbietern implementierte gehört. Einmaligen Empfänger können jede Art von-Adresse, die unterstützt wird von einem der aktiven adressbuchanbietern implementierte besitzen, für die Sitzung. 
  
Einmaligen Empfänger werden in der Regel mit einer Vorlage für ihre speziellen Adresstyp erstellt. Der Adressbuchanbieter, die den Adresstyp unterstützt stellt die Vorlage. Ein Benutzer von einer Clientanwendung gibt die entsprechende Informationen in die Vorlage.
  
MAPI unterstützt Unicode-Zeichenfolgen für die Anzeigenamen, den Adresstyp und die Adressenparameter der **CreateOneOff**.
  
Das Flag MAPI_SEND_NO_RICH_INFO steuert, ob formatierter Text in Rich Text Format (RTF) zusammen mit jeder Nachricht gesendet wird. Die Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung verwendet wird formatierter Text – wird von den meisten Transport Anbietern, unabhängig davon, wie der Empfänger die **PR_SEND_RICH_INFO** -Eigenschaft festgelegt wird gesendet. Dies gilt nicht für die messaging-Clients, die mit Nachrichten zwischen Personen arbeiten. Da TNEF in der Regel zum Senden von benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann nicht unterstützt, es jedoch ein Problem für formularbasierte oder Clients, die eine benutzerdefinierte MAPI-Eigenschaften erfordern. Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI (engl.) verwendet die **CreateOneOff** -Methode, um eine Eintrags-ID für eine Adresse erstellen, die in jeder Adressbuch nicht gefunden werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

