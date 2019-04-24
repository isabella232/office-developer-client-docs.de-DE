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
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348573"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Transport neutrales Encapsulation Format (TNEF)-Objekt, mit dem ein Nachrichtenobjekt für die Verwendung durch Transporte oder Gateways und Nachrichtenspeicher in einen TNEF-Datenstrom codiert oder dekodiert werden kann. Dies ist der Einstiegspunkt für den TNEF-Zugriff. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |TNEF. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Transport Anbieter  <br/> |
   
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
  
> in Übergibt ein Support-Objekt oder übergibt NULL. Bei NULL sollte der _lpAddressBook_ -Parameter ungleich NULL sein. 
    
_lpStream_
  
> in Zeiger auf ein Speicher-Stream-Objekt, wie eine OLE **IStream** -Schnittstelle, die eine Quelle oder ein Ziel für eine TNEF-Stream-Nachricht bereitstellt. 
    
_lpszStreamName_
  
> in Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet. Wenn der Aufrufer das TNEF_ENCODE-Flag ( _ulFlags_ -Parameter) beim Aufruf von **OpenTnefStream**festgelegt hat, muss der Parameter _lpszName_ einen nicht-NULL-Zeiger auf eine nicht-NULL-Zeichenfolge angeben, die aus allen für die Benennung einer Datei gültigen Zeichen besteht. MAPI erlaubt keine Zeichenfolgennamen, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem ihre Verwendung zulässt. Die Größe der für den _lpszName_ -Parameter übergebenen Zeichenfolge darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten. 
    
_ulFlags_
  
> in Bitmaske der Flags, die zum Anzeigen des Modus der Funktion verwendet werden. Die folgenden Flags können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle möglichen Eigenschaften werden in ihre untergeordneten Attribute zugeordnet, aber wenn ein möglicher Datenverlust aufgrund der Konvertierung in ein Down-Level-Attribut vorhanden ist, wird die Eigenschaft auch in den Kapselungs codiert. Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird. TNEF_BEST_DATA ist der Standardwert, wenn keine anderen Modi angegeben werden. 
    
TNEF_COMPATIBILITY 
  
> Bietet Abwärtskompatibilität mit älteren Clientanwendungen. Mit diesem Flag codierte TNEF-Streams ordnen alle möglichen Eigenschaften dem entsprechenden Down-Level-Attribut zu. Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die von Clients der untergeordneten Ebene benötigt werden. 
    
  > [!CAUTION]
  > Dieses Flag ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt des angegebenen Streams wird mit schreibgeschütztem Zugriff geöffnet. Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die spätere Decodierung initialisieren soll.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt des angegebenen Streams wird für Lese-/Schreibzugriff geöffnet. Der Transportanbieter muss dieses Flag festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.
    
TNEF_PURE 
  
> Codiert alle Eigenschaften in die MAPI-Kapselungs Blöcke. Eine reine TNEF-Datei besteht daher höchstens aus den Attributen attMAPIProps, attAttachment, attRenddata und attRecipTable. Dieser Modus eignet sich ideal für den Fall, dass keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> in Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Zielnachricht können durch die Eigenschaften einer codierten Nachricht überschrieben werden.
    
_wKeyVal_
  
> in Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den im Nachrichtentext eingefügten Text Tags zuzuordnen. Dieser Wert sollte für Nachrichten relativ eindeutig sein. 
    
_lpAddressBook_
  
> in Zeiger auf ein Adressbuchobjekt, das zum Abrufen von Adressinformationen für Eintrags-IDs verwendet wird. 
    
_lppTNEF_
  
> Out Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Die **OpenTnefStreamEx** -Funktion ist die empfohlene Ersetzung für [OpenTnefStream](opentnefstream.md), dem ursprünglichen Einstiegspunkt für den TNEF-Zugriff. 
  
Ein von der **OpenTnefStreamEx** -Funktion erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown:: AddRef** auf, um Verweise für das Support-Objekt, das Stream-Objekt und das Message-Objekt hinzuzufügen. Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf an die OLE-Methode **IUnknown:: Release** für das TNEF-Objekt freigeben. 
  
**OpenTnefStreamEx** reserviert und INITIALISIERT ein TNEF-Objekt für den Anbieter, das beim Codieren einer MAPI-Nachricht in eine TNEF-Stream-Nachricht verwendet werden soll. Alternativ kann diese Funktion das Objekt für den Anbieter einrichten, der in nachfolgenden Aufrufen von [ITnef:: ExtractProps](itnef-extractprops.md) zum Decodieren einer TNEF-Stream-Nachricht in eine MAPI-Nachricht verwendet werden soll. Wenn Sie das TNEF-Objekt freigeben und die Sitzung beenden möchten, muss der Transportanbieter die geerbte **IUnknown:: Release** -Methode für das Objekt aufrufen. 
  
Der Basiswert für den _wKeyVal_ -Parameter darf nicht NULL sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx**gleich sein. Verwenden Sie stattdessen Zufallszahlen basierend auf der Systemzeit des Zufallszahlengenerators der Laufzeitbibliothek.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI verwendet die **OpenTnefStreamEx** -Methode, um einen Stream in der TNEF-Datei zu öffnen, damit Eigenschaften extrahiert werden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

