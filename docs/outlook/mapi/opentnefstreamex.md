---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 194558cf39025883e50fceb44e526232ed9a4926
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579425"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein Transport-Neutral Encapsulation Format (TNEF)-Objekt, das zum Codieren oder Decodieren eines Nachrichtenobjekts in einem TNEF-Datenstrom zur Verwendung durch Transporte oder Gateways und Nachrichtenspeicher verwendet werden kann. Dies ist der Einstiegspunkt für den TNEF-Zugriff. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Tnef.h  <br/> |
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
  
> [in] Übergibt ein Unterstützungsobjekt oder übergibt NULL. Wenn NULL, sollte der  _Parameter lpAddressBook_ ungleich NULL sein. 
    
_lpStream_
  
> [in] Zeiger auf ein Speicherdatenstromobjekt, z. B. eine **OLE-IStream-Schnittstelle,** das eine Quelle oder ein Ziel für eine TNEF-Streamnachricht bereitstellt. 
    
_lpszStreamName_
  
> [in] Zeiger auf den Namen des Datenstroms, den das TNEF-Objekt verwendet. Wenn der Aufrufer das TNEF_ENCODE Flag ( _ulFlags-Parameter)_ in seinem Aufruf von **OpenTnefStream** festgelegt hat, muss der  _Parameter lpszName_ einen Nicht-NULL-Zeiger auf eine Zeichenfolge ungleich Null angeben, die aus beliebigen Zeichen besteht, die als gültig für die Benennung einer Datei gelten. MapI lässt keine Zeichenfolgennamen zu, einschließlich der Zeichen "[", "]" oder ":", auch wenn das Dateisystem die Verwendung zulässt. Die Größe der für den  _lpszName-Parameter übergebenen_ Zeichenfolge darf den Wert von MAX_PATH, die maximale Länge einer Zeichenfolge, die einen Pfadnamen enthält, nicht überschreiten. 
    
_ulFlags_
  
> [in] Bitmaske mit Flags, die zum Angeben des Modus der Funktion verwendet werden. Die folgenden Flags können festgelegt werden:
    
TNEF_BEST_DATA 
  
> Alle möglichen Eigenschaften werden ihren Attributen auf der unteren Ebene zugeordnet, aber wenn aufgrund der Konvertierung in ein Attribut auf der unteren Ebene ein möglicher Datenverlust auftritt, wird die Eigenschaft auch in den Kapselungen codiert. Beachten Sie, dass dadurch die Duplizierung von Informationen im TNEF-Stream verursacht wird. TNEF_BEST_DATA ist die Standardeinstellung, wenn keine anderen Modi angegeben sind. 
    
TNEF_COMPATIBILITY 
  
> Bietet Abwärtskompatibilität mit älteren Clientanwendungen. TNEF-Datenströme, die mit diesem Flag codiert sind, ordnen alle möglichen Eigenschaften ihrem entsprechenden Attribut auf der unteren Ebene zu. Dieser Modus bewirkt auch die Standardeinstellung einiger Eigenschaften, die von Clients auf niedriger ebener Ebene benötigt werden. 
    
  > [!CAUTION]
  > Dieses Kennzeichen ist veraltet und sollte nicht verwendet werden. 
  
TNEF_DECODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird mit schreibgeschütztem Zugriff geöffnet. Der Transportanbieter muss dieses Kennzeichen festlegen, wenn die Funktion das Objekt für die nachfolgende Decodierung initialisieren soll.
    
TNEF_ENCODE 
  
> Das TNEF-Objekt im angegebenen Datenstrom wird mit Lese-/Schreibberechtigung geöffnet. Der Transportanbieter muss dieses Kennzeichen festlegen, wenn die Funktion das Objekt für die nachfolgende Codierung initialisieren soll.
    
TNEF_PURE 
  
> Codiert alle Eigenschaften in die MAPI-Kapselungsblöcke. Daher besteht eine "reine" TNEF-Datei höchstens aus den Attributen "attMAPIProps", "attAttachment", "attRenddata" und "attRecipTable". Dieser Modus eignet sich ideal für den Einsatz, wenn keine Abwärtskompatibilität erforderlich ist.
    
_lpMessage_
  
> [in] Zeiger auf ein Nachrichtenobjekt als Ziel für eine decodierte Nachricht mit Anlagen oder eine Quelle für eine codierte Nachricht mit Anlagen. Alle Eigenschaften einer Zielnachricht können von den Eigenschaften einer codierten Nachricht überschrieben werden.
    
_wKeyVal_
  
> [in] Ein Suchschlüssel, den das TNEF-Objekt verwendet, um Anlagen mit den texttags abgleichen, die in den Nachrichtentext eingefügt wurden. Dieser Wert sollte nachrichtenübergreifend relativ eindeutig sein. 
    
_lpAddressBook_
  
> [in] Zeiger auf ein Adressbuchobjekt, mit dem Adressierungsinformationen für Eintragsbezeichner abgerufen werden. 
    
_lppTNEF_
  
> [out] Zeiger auf das neue TNEF-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **OpenTnefStreamEx-Funktion** ist der empfohlene Ersatz für [OpenTnefStream,](opentnefstream.md)den ursprünglichen Einstiegspunkt für TNEF-Zugriff. 
  
Ein von der **OpenTnefStreamEx-Funktion** erstelltes TNEF-Objekt ruft später die OLE-Methode **IUnknown::AddRef** auf, um Verweise für das Supportobjekt, das Stream-Objekt und das Nachrichtenobjekt hinzuzufügen. Der Transportanbieter kann die Verweise für alle drei Objekte mit einem einzigen Aufruf der OLE-Methode **IUnknown::Release** für das TNEF-Objekt freigeben. 
  
**OpenTnefStreamEx** weist dem Anbieter ein TNEF-Objekt zu, das beim Codieren einer MAPI-Nachricht in eine TNEF-Streamnachricht verwendet werden soll, und initialisiert dieses Objekt. Alternativ kann diese Funktion das Objekt für den Anbieter einrichten, das in nachfolgenden Aufrufen von [ITnef::ExtractProps](itnef-extractprops.md) verwendet werden soll, um eine TNEF-Streamnachricht in eine MAPI-Nachricht zu decodieren. Um das TNEF-Objekt freizugeben und die Sitzung zu schließen, muss der Transportanbieter die geerbte **IUnknown::Release-Methode** für das Objekt aufrufen. 
  
Der Basiswert für den  _wKeyVal-Parameter_ darf nicht null sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx** identisch sein. Verwenden Sie stattdessen Zufallszahlen basierend auf der Systemzeit aus dem Zufallszahlengenerator der Laufzeitbibliothek.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI verwendet die **OpenTnefStreamEx-Methode,** um einen Stream in der TNEF-Datei zu öffnen, damit Eigenschaften extrahiert werden können.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

