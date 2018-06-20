---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 52fd844954f41d5d09b5e78f7c23ff6f7469bb43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793327"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Betrifft**: Outlook 
  
Erstellt einen Transport-Neutral Encapsulation Format (TNEF)-Objekt, das zum Ver- oder Entschlüsseln ein Meldungsobjekt in einen Datenstrom von TNEF für die Verwendung von Transporten oder Gateways und Nachrichtenspeicher verwendet werden kann. Dies ist der Einstiegspunkt für TNEF-Zugriff. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transportanbieter  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parameter

_lpvSupport_
  
> [in] Übergibt ein Support-Objekt oder NULL übergibt. Wenn NULL ist, sollte der Parameter _LpAddressBook_ ungleich Null sein. 
    
_lpStream_
  
> [in] Zeiger auf ein Storage Stream-Objekt, wie etwa eine OLE- **IStream** -Schnittstelle, Quelle oder Ziel für eine TNEF-Nachricht Stream bereitstellen. 
    
_lpszStreamName_
  
> [in] Zeiger auf den Namen des Datenstroms, die das TNEF-Objekt verwendet wird. Wenn der Aufrufer das Flag TNEF_ENCODE ( _UlFlags_ -Parameter) in dem Aufruf von **OpenTNEFStream nicht ausgeführt werden**festgelegt, muss den _Wert_ -Parameter einen nicht-Null Zeiger auf eine beliebige Zeichen gültig für eine Datei bestehend ungleich Null-Zeichenfolge angeben. MAPI lässt nicht Zeichenfolgennamen, einschließlich der Zeichen "[", "]", oder ":", auch wenn das Dateisystem ihre Verwendung ermöglicht. Die Größe der für den _Wert_ -Parameter übergebene Zeichenfolge muss den Wert der MAX_PATH, die maximale Länge einer Zeichenfolge, die ein Pfadname enthält, nicht überschreiten. 
    
_ulFlags_
  
> [in] Bitmaske aus Flags verwendet, um den Modus der Funktion anzugeben. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle mögliche Eigenschaften in ihre kompatible Attribute zugeordnet sind, aber bei ein möglichen Datenverlust aufgrund der Konvertierung einer kompatiblen-Attribut vorhanden ist, wird die Eigenschaft auch in der Encapsulations codiert. Beachten Sie, dass dies die Duplizierung von Informationen in der TNEF-Stream verursacht. TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden. 
    
TNEF_COMPATIBILITY 
  
> Stellt die Abwärtskompatibilität mit älteren Clientanwendungen bereit. TNEF-Streams dieses Flag codiert werden alle mögliche Eigenschaften in die entsprechende kompatible Attribut zugeordnet. Dieser Modus wird auch die Standardwerte einiger Eigenschaften, die durch kompatible Clients erforderlich sind. 
    
  > [!CAUTION]
  > Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt im angegebenen Stream wird mit schreibgeschützten Zugriff geöffnet. Der Transportdienst muss dieses Flag festgelegt, wenn die Funktion ist das Objekt für die nachfolgende Decodierung nicht initialisiert werden.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt im angegebenen Stream wird Lese-/Schreibzugriff geöffnet. Der Transportdienst muss dieses Flag festgelegt, wenn die Funktion zum Initialisieren des Objekts für die nachfolgende Codierung ist.
    
TNEF_PURE 
  
> Alle Eigenschaften codiert in die MAPI-Kapselung Blöcke. Aus diesem Grund "reine" TNEF-Datei besteht, höchstens, die Attribute AttMAPIProps, AttAttachment, AttRenddata und AttRecipTable. Dieser Modus ist ideal für die Verwendung, wenn keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> [in] Zeiger auf ein Objekt "Message" als Ziel für eine entschlüsselte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Nachricht Ziel können durch die Eigenschaften einer verschlüsselten Nachricht überschrieben werden soll.
    
_wKeyVal_
  
> [in] Ein Search-Schlüssel, den das TNEF-Objekt wird verwendet, um Anlagen, die Text-Tags in den Nachrichtentext eingefügt übereinstimmen. Dieser Wert sollte über Nachrichten relativ eindeutig sein. 
    
_lpAddressBook_
  
> [in] Zeiger auf eine Adresse Adressbuch-Objekt verwendet, um die Informationen für Eintragsbezeichner Adressierung abrufen. 
    
_lppTNEF_
  
> [out] Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Die **OpenTnefStreamEx** -Funktion ist die empfohlene Ersatz für [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md), den ursprünglichen Einstiegspunkt für TNEF-Zugriff. 
  
Ein TNEF-Objekt, das später durch die Funktion **OpenTnefStreamEx** erstellt Ruft die OLE-Methode **IUnknown:: AddRef** Hinzufügen von Verweisen für den Support-Objekt, das Stream-Objekt und Message-Objekts. Der Transportdienst kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown** für die TNEF-Objekt freigeben. 
  
**OpenTnefStreamEx** reserviert und initialisiert ein TNEF-Objekt für den Anbieter in eine MAPI-Nachricht in ein Stream-Nachricht TNEF-Codierung verwendet. Alternativ kann diese Funktion das Objekt für den Anbieter im nachfolgende Aufrufe von [ITnef::ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in einem MAPI-Nachricht verwenden einrichten. Um die TNEF-Objekts frei, und schließen die Sitzung, muss der Adressbuchhierarchie die geerbte **IUnknown** -Methode für das Objekt aufrufen. 
  
Der Basiswert für den Parameter _wKeyVal_ darf nicht NULL sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx**identisch sein. Verwenden Sie stattdessen Zufallszahlen basierend auf der Systemzeit aus der Laufzeitbibliothek Zufallszahlengenerator.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI (engl.) verwendet die **OpenTnefStreamEx** -Methode, um einen Datenstrom für die TNEF-Datei öffnen, damit Eigenschaften extrahiert werden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

