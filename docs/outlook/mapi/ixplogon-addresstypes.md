---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792873"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Betrifft**: Outlook 
  
Gibt die Typen von Empfängern, die der Adressbuchhierarchie behandelt.
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [out] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lpcAdrType_
  
> [out] Ein Zeiger auf die Anzahl der Einträge in der Matrix, durch den Parameter _LpppszAdrTypeArray_ auf zeigt. 
    
 _lpppszAdrTypeArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen bezeichnet.
    
 _lpcMAPIUID_
  
> [out] Ein Zeiger auf die Anzahl der Einträge in der Matrix, durch den Parameter _LpppUIDArray_ auf zeigt. 
    
 _lpppUIDArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeigern für [MAPIUID](mapiuid.md) -Strukturen, die Empfängertypen zu identifizieren. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Transportdienst angegeben erfolgreich die Typen von Empfängern, die es verarbeiten kann.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die MAPI-Warteschlange Ruft die **IXPLogon::AddressTypes** -Methode auf, unmittelbar nachdem ein Transportdienstes aus einen Anruf an die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode zurückgegeben, damit der Adressbuchhierarchie angeben kann, welche Arten von Empfängern verarbeitet. Um dies darauf hinzuweisen, sollte der Adressbuchhierarchie in der _LpppszAdrTypeArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen übergeben oder wieder in den _LpppUIDArray_ -Parameter einen Zeiger auf ein Array von Zeigern für **MAPIUID** übergeben Strukturen oder Werte in beiden Parametern übergeben. 
  
Für verschiedene Identification Prozesse werden diese beiden Arrays verwendet. MAPI- und die MAPI-Warteschlange können Sie die Strukturen [MAPIUID](mapiuid.md) im Array _LpppUIDArray_ verwenden, um diese Empfänger-Eintragsbezeichner identifizieren, die direkt mit der Adressbuchhierarchie oder mit der messaging-System mit dem der Adressbuchhierarchie verbindet behandelt werden . MAPI- weder die MAPI-Warteschlange erweitert Adressen mithilfe von Eintragsbezeichner in keiner dieser **MAPIUID** Strukturen enthalten; Diese Strukturen dienen nur zur Identifizierung der Empfängertyp. 
  
Die MAPI-Warteschlange verwendet jede der Zeichenfolgen in der _LpppszAdrTypeArray_ -Parameter für einen Vergleichstest bei der Festlegung, welche Adressbuchhierarchie welche Empfänger für eine ausgehende Nachricht behandelt werden sollen. Wenn der Empfänger einer Nachricht **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft eine Zeichenfolge übereinstimmt, die eines der messaging-Adresstypen identifiziert, die der Adressbuchhierarchie bereitstellt, kann der Anbieter die Nachricht an diesen Empfänger übermitteln.
  
Wenn mehrere Transportanbieter den gleichen Typ des Empfängers verarbeitet werden können, wählt MAPI ein Transportdienstes basierend auf der Transport Prioritätsreihenfolge aus, die in der Clientanwendung Profil angegeben. Um festzustellen, welche Adressbuchhierarchie verwenden, überprüft die MAPI-Warteschlange alle Anbieter angegeben **MAPIUID** Strukturen in Prioritätsreihenfolge aus, und klicken Sie dann alle Anbieter angegebene Adresse Geben Sie Werte in Prioritätsreihenfolge aus. Der erste Transportdienst auf einen bestimmten Empfänger in diese Überprüfung übereinstimmen Ruft die erste Möglichkeit, diesen Empfänger zu verarbeiten. Wenn dieses Anbieters den Empfänger nicht behandelt wird, wird die MAPI-Warteschlange die Überprüfung ein Transportdienstes für jeden Empfänger noch nicht verarbeitet finden fortgesetzt. Die Überprüfung wird fortgesetzt, bis keine weiteren Treffer gefunden werden, an welcher Stelle ein Unzustellbarkeitsbericht für alle Empfänger generiert wird, die nicht bearbeitet wurde. 
  
Wenn der Anbieter immer einen bestimmten Satz von Empfängertypen unterstützt, können der Adresstyp und **MAPIUID** Arrays, die der Adressbuchhierarchie übergeben statisch sein. Wenn der Adressbuchhierarchie diese Arrays dynamisch erstellt wurde, können sie Speicher mithilfe des Support-Objekts, das zuvor im Aufruf **TransportLogon**, übergeben wurde, obwohl dies nicht erforderlich ist.
  
Der Speicher für den Adresstyp und **MAPIUID** Arrays verwendet sollte erst nach dem letzten Aufruf der [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) -Methode zugewiesenen bleiben bei der Adressbuchhierarchie den Arbeitsspeicher bei Bedarf freigegeben werden kann. Der Transportdienst sollten nicht den Inhalt dieser Arrays ändern, nachdem ein Wert aus dem Aufruf **TransportLogoff** zurückgegeben. 
  
Ein Transportanbieter, der jeden Empfänger behandeln kann kann im Parameter _LpppszAdrTypeArray_ NULL zurückgegeben. Transportanbieter für LAN-basierte messaging-Systemen, die einen zentralen Server ausgehende Nachrichten an verschiedenen foreign Nachrichtensysteme häufig übermitteln verwenden hierzu. Diese Art der Adressbuchhierarchie zuletzt in den MAPI- und MAPI-installiert werden soll Warteschlange Prioritätsreihenfolge aus der Transportanbieter im Profil. 
  
Ein Transportdienstes, das nicht unterstützt werden ausgehende Nachrichten, die versandt werden, basierend auf den Adresstyp sollte in _LpppszAdrTypeArray_eine einzelne Zeichenfolge der Länge Null zurückgegeben. Wenn ein Transportdienstes keine Empfängertypen unterstützt, sollten sie NULL für die **MAPIUID** -Struktur und eine leere Zeichenfolge für den Adresstyp übergeben. Transportanbieter dieses Typs werden am häufigsten verwendet, um eine Nachricht Präprozessor zu installieren. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

