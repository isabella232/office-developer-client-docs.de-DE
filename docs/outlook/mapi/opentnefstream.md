---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423958"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wird von einem Transportanbieter aufgerufen, um eine MAPI Transport Neutral Encapsulation Format (TNEF)-Sitzung zu initiieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Tnef.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transportanbieter  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parameter

_lpvSupport_
  
> [in] Übergibt ein Supportobjekt oder null. 
    
_lpStream_
  
> [in] Zeiger auf eine OLE **IStream-Schnittstelle** des Speicherdatenstromobjekts, die eine Quelle oder ein Ziel für eine TNEF-Streamnachricht bietet. 
    
_lpszStreamName_
  
> [in] Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet. Wenn der Aufrufer das TNEF_ENCODE-Flag ( _ulFlags-Parameter)_ in seinem Aufruf von **OpenTnefStream** festgelegt hat, muss der  _lpszName-Parameter_ einen Nicht-Null-Zeiger auf eine Nicht-Null-Zeichenfolge angeben, die aus allen Zeichen besteht, die für die Benennung einer Datei als gültig gelten. MAPI lässt keine Zeichenfolgennamen zu, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem die Verwendung zulässt. Die Größe der zeichenfolge, die für  _lpszName_ übergeben wird, darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten. 
    
_ulFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um den Modus der Funktion anzugeben. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle möglichen Eigenschaften werden ihren Attributen auf der ebeneren Ebene zugeordnet, aber wenn aufgrund der Konvertierung in ein Down-Level-Attribut ein möglicher Datenverlust besteht, wird die Eigenschaft auch in den Kapselungen codiert. Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird. TNEF_BEST_DATA ist die Standardeinstellung, wenn keine anderen Modi angegeben werden. 
    
TNEF_COMPATIBILITY 
  
> Bietet Abwärtskompatibilität mit den älteren Clientanwendungen. Mit diesem Flag codierte TNEF-Datenströme ordnen alle möglichen Eigenschaften ihrem entsprechenden Attribut auf unterer Ebene zu. Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die für Clients auf ebener Ebene erforderlich sind. 
    
  > [!CAUTION]
  > Dieses Flag ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird mit schreibgeschützten Zugriff geöffnet. Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Decodierung initialisieren soll.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird für Lese-/Schreibberechtigungen geöffnet. Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.
    
TNEF_PURE 
  
> Codiert alle Eigenschaften in die MAPI-Kapselungsblöcke. Daher besteht eine "reine" TNEF-Datei aus attMAPIProps, attAttachment, attRenddata und attRecipTable. Dieser Modus eignet sich ideal, wenn keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> [in] Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Zielnachricht können von den Eigenschaften einer codierten Nachricht überschrieben werden.
    
_wKey_
  
> [in] Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den im Nachrichtentext eingefügten Texttags zu versehen. Dieser Wert sollte nachrichtenübergreifend relativ eindeutig sein.
    
_lppTNEF_
  
> [out] Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Ein von der **OpenTnefStream-Funktion** erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown::AddRef** auf, um Verweise für das Supportobjekt, das Stream-Objekt und das Message-Objekt hinzuzufügen. Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown::Release für** das TNEF-Objekt los. 
  
**OpenTnefStream** weist eine **ITnef-Schnittstelle** des TNEF-Objekts zu, die vom Anbieter zum Codieren einer **IMessage-Schnittstelle** für MAPI-Nachrichten in eine TNEF-Streamnachricht verwendet werden soll. Alternativ kann die Funktion das Objekt für den Anbieter für nachfolgende Aufrufe von [ITnef::ExtractProps](itnef-extractprops.md) einrichten, um eine TNEF-Streamnachricht in eine MAPI-Nachricht zu decodieren. Um das TNEF-Objekt frei zu geben und die Sitzung zu schließen, muss der Transportanbieter die geerbte **IUnknown::Release-Methode** für das Objekt aufrufen. 
  
Diese Funktion ist der ursprüngliche Einstiegspunkt für den TNEF-Zugriff und wurde durch [OpenTnefStreamEx](opentnefstreamex.md) ersetzt, wird jedoch weiterhin zur Kompatibilität für Benutzer verwendet, die bereits TNEF verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

