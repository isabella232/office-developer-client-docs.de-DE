---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791999"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Betrifft**: Outlook 
  
Führt Namensresolution Eintragsbezeichner an Empfänger in der Empfängerliste zuweisen.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des ein Dialogfeld angezeigt wird, wenn angegeben, den Benutzer zum Auflösen der Mehrdeutigkeit,.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die verschiedene Aspekte des Prozesses Lösung steuern. Die folgenden Kennzeichen können festgelegt werden:
    
AB_UNICODEUI
  
> Gibt an, dass diese _LpszNewEntryTitle_ UNICODE-Zeichenfolge ist. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld, um die Aufforderung des Benutzers für zusätzliche Namensinformationen der Lösung an. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt. 
    
PARAMETER MAPI_UNICODE 
  
> Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstelle von PT_STRING8 sein sollte. 
    
 _lpszNewEntryTitle_
  
> [in] Ein Zeiger auf den Text für den Titel des Steuerelements in dem Dialogfeld, das den Benutzer auffordert, einen Empfänger eingeben. Der Titel variiert je nach den Typ des Empfängers. Der Parameter _LpszNewEntryTitle_ kann NULL sein. 
    
 _lpAdrList_
  
> [in Out] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die enthält die Liste der Namen der Empfänger aufgelöst werden. Diese Struktur **ADRLIST** kann von der [IAddrBook::Address](iaddrbook-address.md) -Methode erstellt werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Vorgang der Lösung war erfolgreich.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Mindestens ein Empfänger im Parameter _LpAdrList_ abgeglichen mehr als einen Eintrag im Adressbuch. Dieser Wert wird in der Regel zurückgegeben, wenn das Flag MAPI_DIALOG verhindern der Anzeige eines Dialogfelds festgelegt ist. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens ein Empfänger in der _LpAdrList_ -Parameter kann nicht aufgelöst werden. Dieser Wert wird in der Regel zurückgegeben, wenn das Flag MAPI_DIALOG verhindern der Anzeige eines Dialogfelds festgelegt ist. 
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen Sie die **ResolveName** -Methode, um die Namen Lösung zu initiieren. Ein nicht aufgelöster Eintrag ist ein Eintrag, der eine Eintrags-ID oder -Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) noch nicht vorhanden ist.
  
 **ResolveName** erfolgt über den folgenden Vorgang für jeden nicht aufgelösten Eintrag in der Adressliste im _LpAdrList_ -Parameter übergeben wird. 
  
1. Wenn das Format der SMTP-Adresse des Empfängers Adresstyp entspricht ( _Displayname_@ _domain.top-Level-Domäne_), **ResolveName** weist ihm einen Eingangs-Bezeichner. 
    
2. Für jeden Container in der Eigenschaft **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) Ruft **ResolveName** die [IABContainer](iabcontainer-resolvenames.md) -Methode. **ResolveNames** versucht, den Anzeigenamen des jeden nicht aufgelösten Empfänger mit dem Anzeigenamen zuzuordnen, die auf eine der zugehörigen Einträge gehört. 
    
3. Wenn ein Container **ResolveNames**nicht unterstützt, schränkt **ResolveName** Inhaltstabelle des Containers mithilfe einer eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Diese Einschränkung bewirkt, dass den Container zum Ausführen eines "am besten erraten" Typs der Suche aus, um einen übereinstimmenden Empfänger zu suchen. Von allen Containern müssen der **PR_ANR** eigenschaftseinschränkung unterstützen. 
    
4. Wenn ein Container ein Empfängers, das mehrere Namen entspricht zurückgegeben, im **ResolveName** ein Dialogfeld angezeigt, wenn das Flag MAPI_DIALOG festgelegt ist, dem den Benutzer den gewünschten Namen auswählen können. 
    
5. Wenn alle Container in der Eigenschaft **PR_AB_SEARCH_PATH** aufgerufen wurde und keine Übereinstimmung gefunden wurde, bleibt der Empfänger nicht aufgelöst. 
    
Wenn Sie einen oder mehrere Empfänger nicht aufgelöst werden, gibt **ResolveName** MAPI_E_NOT_FOUND zurück. Wenn Sie einen oder mehrere Empfänger war mehrdeutig Lösung, die mit einem Dialogfeld nicht aufgelöst werden konnte, oder da das Flag MAPI_DIALOG nicht festgelegt wurde, **ResolveName** MAPI_E_AMBIGUOUS_RECIP gibt. Wenn einige der Empfänger nicht eindeutig sind und einige nicht aufgelöst werden kann, können **ResolveName** entweder Fehlerwert zurück. 
  
Wenn Sie ein Namen aufgelöst werden kann, kann der Client eine einmalige Adresse erstellen, die ein speziell formatierte Adresse und Eintrags-ID verfügt. Weitere Informationen zum Format von Eintragsbezeichner einmaligen finden Sie unter [Einmaligen-Eintragsbezeichner](one-off-entry-identifiers.md). Weitere Informationen zum Format von einmal-Adressen finden Sie unter [Einmal-Adressen](one-off-addresses.md).
  
MAPI unterstützt Unicode-Zeichenfolgen für die **ADRLIST** und die neuen Eintrag Titel Parameter **ResolveName**. Wenn Sie die Option MAPI_UNICODE festlegen, werden die folgenden Eigenschaften als Typ PT_UNICODE in die Strukturen [ADRENTRY](adrentry.md) zurückgegeben: 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Die **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md))-Eigenschaft wird jedoch immer zurückgegeben, PT_STRING8 eingeben.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI (engl.) verwendet die **ResolveName** -Methode, um eine einmal Adresse aufzulösen, vor dem Hinzufügen zu einer Nachricht.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI (engl.) verwendet die **ResolveName** -Methode nach dem Anzeigenamen eines Adresseintrags Adressbuch nachzuschlagen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

