---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bcda2b9445fca40ba2f67e25b3d6ae7a949ceb52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571381"
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
  
> [in] Übergibt ein Unterstützungsobjekt oder übergibt NULL. 
    
_lpStream_
  
> [in] Zeiger auf eine OLE **IStream-Schnittstelle** eines Speicherdatenstromobjekts, die eine Quelle oder ein Ziel für eine TNEF-Streamnachricht bereitstellt. 
    
_lpszStreamName_
  
> [in] Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet. Wenn der Aufrufer das TNEF_ENCODE Flag ( _ulFlags-Parameter)_ in seinem Aufruf von **OpenTnefStream** festgelegt hat, muss der  _Parameter lpszName_ einen Nicht-NULL-Zeiger auf eine Zeichenfolge ungleich Null angeben, die aus beliebigen Zeichen besteht, die als gültig für die Benennung einer Datei gelten. MapI lässt keine Zeichenfolgennamen zu, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem die Verwendung zulässt. Die Größe der für  _lpszName übergebenen_ Zeichenfolge darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten. 
    
_ulFlags_
  
> [in] Bitmaske mit Flags, die zum Angeben des Modus der Funktion verwendet werden. Die folgenden Flags können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle möglichen Eigenschaften werden ihren Attributen auf der unteren Ebene zugeordnet, aber wenn aufgrund der Konvertierung in ein Attribut auf der unteren Ebene ein möglicher Datenverlust auftritt, wird die Eigenschaft auch in den Kapselungen codiert. Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird. TNEF_BEST_DATA ist die Standardeinstellung, wenn keine anderen Modi angegeben sind. 
    
TNEF_COMPATIBILITY 
  
> Bietet Abwärtskompatibilität mit den älteren Clientanwendungen. TNEF-Datenströme, die mit diesem Flag codiert sind, ordnen alle möglichen Eigenschaften ihrem entsprechenden Attribut auf der unteren Ebene zu. Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die von Clients auf niedriger ebener Ebene benötigt werden. 
    
  > [!CAUTION]
  > Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird mit schreibgeschütztem Zugriff geöffnet. Der Transportanbieter muss dieses Kennzeichen festlegen, wenn die Funktion das Objekt für die nachfolgende Decodierung initialisieren soll.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird mit Lese-/Schreibberechtigung geöffnet. Der Transportanbieter muss dieses Kennzeichen festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.
    
TNEF_PURE 
  
> Codiert alle Eigenschaften in die MAPI-Kapselungsblöcke. Daher besteht eine "reine" TNEF-Datei höchstens aus attMAPIProps, attAttachment, attRenddata und attRecipTable. Dieser Modus eignet sich ideal für den Einsatz, wenn keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> [in] Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Zielnachricht werden möglicherweise von den Eigenschaften einer codierten Nachricht überschrieben.
    
_wKey_
  
> [in] Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den texttags abgleichen, die in den Nachrichtentext eingefügt wurden. Dieser Wert sollte nachrichtenübergreifend relativ eindeutig sein.
    
_lppTNEF_
  
> [out] Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein von der **OpenTnefStream-Funktion** erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown::AddRef** auf, um Verweise für das Supportobjekt, das Streamobjekt und das Nachrichtenobjekt hinzuzufügen. Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown::Release** für das TNEF-Objekt freigeben. 
  
**OpenTnefStream** weist eine **ITnef-Schnittstelle** des TNEF-Objekts zu und initialisiert sie, damit der Anbieter eine MAPI-Nachrichten-IMessage-Schnittstelle in eine TNEF-Streamnachricht codiert.  Alternativ kann die Funktion das Objekt für den Anbieter einrichten, das in nachfolgenden Aufrufen von [ITnef::ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Streamnachricht in eine MAPI-Nachricht verwendet werden soll. Um das TNEF-Objekt freizugeben und die Sitzung zu schließen, muss der Transportanbieter die geerbte **IUnknown::Release-Methode** für das Objekt aufrufen. 
  
Diese Funktion ist der ursprüngliche Einstiegspunkt für den TNEF-Zugriff und wurde durch [OpenTnefStreamEx](opentnefstreamex.md) ersetzt, wird jedoch weiterhin für kompatibilitätsbedingt für diejenigen verwendet, die TNEF bereits verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

