---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3423391ce6744f7a21bed337778fd8a76aa15d4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587811"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Empfängertypen zurück, die der Transportanbieter verarbeitet.
  
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
  
> [out] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lpcAdrType_
  
> [out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die der  _parameter lpppszAdrTypeArray_ verweist. 
    
 _lpppszAdrTypeArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen identifizieren.
    
 _lpcMAPIUID_
  
> [out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die durch den  _Parameter lpppUIDArray_ verwiesen wird. 
    
 _lpppUIDArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeigern auf [MAPIUID-Strukturen,](mapiuid.md) die Empfängertypen identifizieren. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat die Empfängertypen, die er verarbeiten kann, erfolgreich angegeben.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der MAPI-Spooler ruft die **IXPLogon::AddressTypes-Methode** auf, unmittelbar nachdem ein Transportanbieter von einem Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) zurückgegeben wurde, damit der Transportanbieter angeben kann, welche Empfängertypen er behandelt. Um dies anzugeben, sollte der Transportanbieter im _lpppszAdrTypeArray-Parameter_ einen Zeiger an ein Array von Zeigern auf Zeichenfolgen übergeben oder einen Zeiger an ein Array von Zeigern an **MAPIUID-Strukturen** im _LpppUIDArray-Parameter_ zurückgeben oder Werte in beiden Parametern übergeben. 
  
Diese beiden Arrays werden für unterschiedliche Identifikationsprozesse verwendet. DIE MAPI und der MAPI-Spooler verwenden die [MAPIUID-Strukturen](mapiuid.md) im  _LpppUIDArray-Array,_ um die Empfängereintrags-IDs zu identifizieren, die direkt vom Transportanbieter oder vom Messagingsystem verarbeitet werden, mit dem der Transportanbieter eine Verbindung herstellt. Weder die MAPI noch der MAPI-Spooler erweitert Adressen mithilfe von Eintragsbezeichnern, die in diesen **MAPIUID-Strukturen** enthalten sind. Diese Strukturen werden nur für die Empfängertypidentifikation verwendet. 
  
Der MAPI-Spooler verwendet die einzelnen Zeichenfolgen im  _Parameter lpppszAdrTypeArray_ für einen Vergleichstest, wenn er entscheidet, welcher Transportanbieter welche Empfänger für eine ausgehende Nachricht behandeln soll. Wenn die **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) -Eigenschaft eines Nachrichtenempfängers genau mit einer Zeichenfolge übereinstimmt, die einen der vom Transportanbieter bereitgestellten Messagingadressentypen identifiziert, kann der Anbieter die Nachricht an diesen Empfänger übermitteln.
  
Wenn mehrere Transportanbieter den gleichen Empfängertyp verarbeiten können, wählt mapi basierend auf der im Profil der Clientanwendung angegebenen Transportprioritätsreihenfolge einen Transportanbieter aus. Um zu bestimmen, welcher Transportanbieter verwendet werden soll, überprüft der MAPI-Spooler alle vom Anbieter angegebenen **MAPIUID-Strukturen** in der Reihenfolge der Priorität und dann alle vom Anbieter angegebenen Adresstypwerte in der Prioritätsreihenfolge. Der erste Transportanbieter, der einen bestimmten Empfänger in dieser Überprüfung abgleicht, erhält die erste Möglichkeit, diesen Empfänger zu behandeln. Wenn dieser Anbieter den Empfänger nicht verarbeitet, setzt der MAPI-Spooler die Überprüfung fort, um einen Transportanbieter für einen empfänger zu finden, der noch nicht behandelt wurde. Die Überprüfung wird fortgesetzt, bis keine weiteren Übereinstimmungen gefunden werden. An diesem Punkt wird ein Nicht-Empfängerbericht generiert, der nicht behandelt wurde. 
  
Wenn der Anbieter immer einen bestimmten Satz von Empfängertypen unterstützt, können der Adresstyp und die **MAPIUID-Arrays,** die der Transportanbieter übergeben hat, statisch sein. Wenn der Transportanbieter diese Arrays dynamisch erstellt, kann er Speicher mithilfe des Supportobjekts zuordnen, das zuvor beim Aufruf von **TransportLogon** übergeben wurde, obwohl dies nicht erforderlich ist.
  
Der für den Adresstyp und **die MAPIUID-Arrays** verwendete Arbeitsspeicher sollte bis zum letzten Aufruf der [IXPLogon::TransportLogoff-Methode](ixplogon-transportlogoff.md) zugeordnet bleiben, wobei der Transportanbieter den Speicher bei Bedarf freigeben kann. Der Transportanbieter sollte den Inhalt dieser Arrays nicht ändern, nachdem er vom **TransportLogoff-Aufruf** zurückgegeben wurde. 
  
Ein Transportanbieter, der jeden Empfängertyp verarbeiten kann, kann NULL im  _LpppszAdrTypeArray-Parameter_ zurückgeben. Transportanbieter für LAN-basierte Messagingsysteme, die einen zentralen Server verwenden, um ausgehende Nachrichten an verschiedene Fremdnachrichtensysteme zu übermitteln, tun dies in der Regel. Dieser Transportanbietertyp sollte zuletzt in der MAPI- und MAPI-Spooler-Prioritätsreihenfolge der Transportanbieter im Profil installiert werden. 
  
Ein Transportanbieter, der ausgehende Nachrichten, die basierend auf dem Adresstyp an ihn gesendet werden, nicht unterstützt, sollte eine einzelne leere Zeichenfolge in  _lpppszAdrTypeArray_ zurückgeben. Wenn ein Transportanbieter keine Empfängertypen unterstützt, sollte null für die **MAPIUID-Struktur** und eine leere Zeichenfolge für den Adresstyp übergeben werden. Transportanbieter dieses Typs werden am häufigsten zum Installieren eines Nachrichtenpräprozessors verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

