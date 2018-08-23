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
ms.openlocfilehash: c5abd3a80a9736a4d71525805e4bc38289975c34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577807"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aufgerufen von eines Transportdienstes So initiieren Sie eine Sitzung MAPI Transport Neutral Encapsulation Format (TNEF). 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
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
  
> [in] Übergibt ein Support-Objekt oder NULL übergibt. 
    
_lpStream_
  
> [in] Zeiger auf einen Speicher Stream-Objekt OLE **IStream** Schnittstelle Bereitstellen von Quelle oder Ziel für eine Nachricht der TNEF-Stream. 
    
_lpszStreamName_
  
> [in] Zeiger auf den Namen des Datenstroms, die das TNEF-Objekt verwendet wird. Wenn der Aufrufer das Flag TNEF_ENCODE ( _UlFlags_ -Parameter) in dem Aufruf von **OpenTNEFStream nicht ausgeführt werden**festgelegt, muss den _Wert_ -Parameter einen nicht-Null Zeiger auf eine beliebige Zeichen gültig für eine Datei bestehend ungleich Null-Zeichenfolge angeben. MAPI lässt nicht Zeichenfolgennamen, einschließlich der Zeichen "[", "]", oder ":", auch wenn das Dateisystem ihre Verwendung ermöglicht. Die Größe der für _Wert_ übergebene Zeichenfolge muss den Wert der MAX_PATH, die maximale Länge einer Zeichenfolge, die ein Pfadname enthält, nicht überschreiten. 
    
_ulFlags_
  
> [in] Bitmaske aus Flags verwendet, um den Modus der Funktion anzugeben. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle mögliche Eigenschaften in ihre kompatible Attribute zugeordnet sind, aber bei ein möglichen Datenverlust aufgrund der Konvertierung einer kompatiblen-Attribut vorhanden ist, wird die Eigenschaft auch in der Encapsulations codiert. Beachten Sie, dass dies die Duplizierung von Informationen in der TNEF-Stream verursacht. TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden. 
    
TNEF_COMPATIBILITY 
  
> Stellt die Abwärtskompatibilität mit älteren Client Clientanwendungen bereit. TNEF-Streams dieses Flag codiert werden alle mögliche Eigenschaften in die entsprechende kompatible Attribut zugeordnet. Dieser Modus wird auch die Standardwerte einiger Eigenschaften, die durch kompatible Clients erforderlich sind. 
    
  > [!CAUTION]
  > Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt im angegebenen Stream wird mit schreibgeschützten Zugriff geöffnet. Der Transportdienst muss dieses Flag festgelegt, wenn sie die Funktion zum Initialisieren des Objekts für die nachfolgende Decodierung möchte.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt im angegebenen Stream wird Lese-/Schreibzugriff geöffnet. Der Transportdienst muss dieses Flag festgelegt, wenn sie die Funktion zum Initialisieren des Objekts für die nachfolgende Codierung möchte.
    
TNEF_PURE 
  
> Alle Eigenschaften codiert in die MAPI-Kapselung Blöcke. Aus diesem Grund "reine" TNEF-Datei besteht aus, an die meisten, AttMAPIProps AttAttachment, AttRenddata, und AttRecipTable. Dieser Modus ist ideal für die Verwendung, wenn keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> [in] Zeiger auf ein Objekt "Message" als Ziel für eine entschlüsselte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Nachricht Ziel möglicherweise durch die Eigenschaften einer verschlüsselten Nachricht überschrieben werden soll.
    
_wKey_
  
> [in] Ein Search-Schlüssel, den das TNEF-Objekt wird verwendet, um Anlagen, die Text-Tags in den Nachrichtentext eingefügt übereinstimmen. Dieser Wert sollte über Nachrichten relativ eindeutig sein.
    
_lppTNEF_
  
> [out] Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Ein TNEF-Objekt von der Funktion **OpenTNEFStream nicht ausgeführt werden** später erstellt Ruft die OLE-Methode **IUnknown:: AddRef** Hinzufügen von Verweisen für den Support-Objekt, das Stream-Objekt und Message-Objekts. Der Transportdienst kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown** für die TNEF-Objekt freigeben. 
  
**OpenTNEFStream nicht ausgeführt werden** reserviert und initialisiert TNEF-Objektschnittstelle **ITnef** für den Anbieter in einer MAPI-Nachricht **IMessage** -Schnittstelle in einem Stream TNEF-Nachricht-Codierung verwendet. Alternativ kann das Objekt für den Anbieter im nachfolgende Aufrufe von [ITnef::ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in einem MAPI-Nachricht verwenden die Funktion einrichten. Um die TNEF-Objekts frei, und schließen die Sitzung, muss der Adressbuchhierarchie die geerbte **IUnknown** -Methode für das Objekt aufrufen. 
  
Diese Funktion ist der ursprüngliche Einstiegspunkt für den Zugriff von TNEF und wurde ersetzt durch [OpenTnefStreamEx](opentnefstreamex.md) aber weiterhin für die Kompatibilität für die Verwendung von TNEF bereits verwendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

