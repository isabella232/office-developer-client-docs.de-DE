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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357211"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Empfängertypen zurück, die vom Transportanbieter verarbeitet werden.
  
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
  
> Out Eine Bitmaske von Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lpcAdrType_
  
> Out Ein Zeiger auf die Anzahl der Einträge im Array, auf die durch den _lpppszAdrTypeArray_ -Parameter verwiesen wird. 
    
 _lpppszAdrTypeArray_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen identifizieren.
    
 _lpcMAPIUID_
  
> Out Ein Zeiger auf die Anzahl der Einträge im Array, auf die durch den _lpppUIDArray_ -Parameter verwiesen wird. 
    
 _lpppUIDArray_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Zeigern auf [MAPIUID](mapiuid.md) -Strukturen, die Empfängertypen identifizieren. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat erfolgreich die Empfängertypen angegeben, die er verarbeiten kann.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der MAPI-Spooler Ruft die **IXPLogon:: AddressTypes** -Methode unmittelbar auf, nachdem ein Transportanbieter von einem Aufruf der [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode zurückgegeben hat, sodass der Transportanbieter anzeigen kann, welche Empfängertypen er verarbeitet. Um dies anzugeben, sollte der Transportanbieter zurückgeben, in der _lpppszAdrTypeArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen oder zurückgeben Sie den _lpppUIDArray_ -Parameter einen Zeiger auf ein Array von Zeigern auf **MAPIUID** Strukturen oder übergeben Sie Werte in beiden Parametern. 
  
Diese beiden Arrays werden für verschiedene identifizierungsprozesse verwendet. MAPI und der MAPI-Spooler verwenden die [MAPIUID](mapiuid.md) -Strukturen im _lpppUIDArray_ -Array, um die Empfänger Eintrags-IDs zu identifizieren, die direkt vom Transportanbieter oder vom Messagingsystem verarbeitet werden, mit dem der Transportanbieter eine Verbindung herstellt. . Weder MAPI noch der MAPI-Spooler erweitern Adressen mithilfe von Eintrags-IDs, die in einer dieser **MAPIUID** -Strukturen enthalten sind; Diese Strukturen werden nur zur Identifizierung von Empfängertypen verwendet. 
  
Der MAPI-Spooler verwendet jede der Zeichenfolgen im _lpppszAdrTypeArray_ -Parameter für einen Vergleichstest, wenn er entscheidet, welcher Transportanbieter welche Empfänger für eine ausgehende Nachricht behandeln soll. Wenn die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft eines Nachrichtenempfängers genau mit einer Zeichenfolge übereinstimmt, die einen der vom Transportanbieter bereitgestellten Messaging Adresstypen identifiziert, kann der Anbieter die Nachricht an diesen Empfänger übermitteln.
  
Wenn mehrere Transportanbieter denselben Empfängertyp verarbeiten können, wählt MAPI einen Transportanbieter basierend auf der im Profil der Clientanwendung angegebenen Transport Prioritätsreihenfolge aus. Um zu bestimmen, welcher Transportanbieter verwendet werden soll, scannt der MAPI-Spooler alle vom Anbieter angegebenen **MAPIUID** -Strukturen in der Prioritätsreihenfolge und dann alle vom Anbieter angegebenen Adresstyp Werte in der Prioritätsreihenfolge. Der erste Transportanbieter, der einem bestimmten Empfänger bei dieser Überprüfung entspricht, erhält die erste Gelegenheit, diesen Empfänger zu behandeln. Wenn dieser Anbieter den Empfänger nicht verarbeitet, setzt der MAPI-Spooler die Überprüfung fort, um einen Transportanbieter für einen Empfänger zu finden, der noch nicht behandelt wurde. Die Überprüfung wird fortgesetzt, bis keine weiteren Übereinstimmungen gefunden werden, an welcher Stelle ein Unzustellbarkeitsbericht für einen Empfänger generiert wird, der nicht behandelt wurde. 
  
Wenn der Anbieter eine bestimmte Gruppe von Empfängertypen immer unterstützt, können der Adresstyp und die **MAPIUID** -Arrays, die der Transportanbieter übergeben hat, statisch sein. Wenn der Transportanbieter diese Arrays dynamisch erstellt, kann er Arbeitsspeicher mithilfe des Support-Objekts zuweisen, das zuvor im Aufruf an **TransportLogon**übergeben wurde, obwohl dies nicht erforderlich ist.
  
Der für den Adresstyp und **MAPIUID** -Arrays verwendete Speicher sollte bis zum letzten Aufruf der [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) -Methode reserviert werden, zu der Zeit, zu der der Transportanbieter den Arbeitsspeicher freigeben kann, falls erforderlich. Der Transportanbieter sollte den Inhalt dieser Arrays nicht ändern, nachdem er vom **TransportLogoff** -Aufruf zurückgegeben wurde. 
  
Ein Transportanbieter, der einen beliebigen Empfängertyp verarbeiten kann, kann im _lpppszAdrTypeArray_ -Parameter NULL zurückgeben. Transport Anbieter für LAN-basierte Messagingsysteme, die einen zentralen Server verwenden, um ausgehende Nachrichten an verschiedene fremd Nachrichtensysteme zuzustellen, tun dies häufig. Dieser Transport Anbietertyp sollte zuletzt in der MAPI-und MAPI-Spooler-Prioritätsreihenfolge der Transportanbieter im Profil installiert werden. 
  
Ein Transportanbieter, der ausgehende Nachrichten, die basierend auf dem Adresstyp an ihn gesendet werden, nicht unterstützt, sollte eine einzelne leere Zeichenfolge in _lpppszAdrTypeArray_zurückgeben. Wenn ein Transportanbieter keine Empfängertypen unterstützt, sollte er NULL für die **MAPIUID** -Struktur und eine leere Zeichenfolge für den Adresstyp überschreiten. Transport Anbieter dieses Typs werden am häufigsten für die Installation eines nachrichtenpräprozessors verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

