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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435376"
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
  
> [out] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die zurückgegebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lpcAdrType_
  
> [out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die der  _lpppszAdrTypeArray-Parameter_ verweist. 
    
 _lpppszAdrTypeArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeichenfolgen, die Empfängertypen identifizieren.
    
 _lpcMAPIUID_
  
> [out] Ein Zeiger auf die Anzahl der Einträge im Array, auf die der  _lpppUIDArray-Parameter_ verweist. 
    
 _lpppUIDArray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Zeigern auf [MAPIUID-Strukturen,](mapiuid.md) die Empfängertypen identifizieren. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Transportanbieter hat die Empfängertypen, die er verarbeiten kann, erfolgreich angegeben.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der MAPI-Spooler ruft die **IXPLogon::AddressTypes-Methode** unmittelbar nach der Rückgabe eines Transportanbieters von einem Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) auf, damit der Transportanbieter angeben kann, welche Empfängertypen er verarbeitet. Um dies anzugeben, sollte der Transportanbieter im  _lpppszAdrTypeArray-Parameter_ einen Zeiger auf ein Array von Zeigern auf Zeichenfolgen übergeben oder im  _lpppUIDArray-Parameter_ einen Zeiger an ein Array von Zeigern an **MAPIUID-Strukturen** übergeben oder Werte in beiden Parametern übergeben. 
  
Diese beiden Arrays werden für verschiedene Identifikationsprozesse verwendet. MAPI und der MAPI-Spooler verwenden die [MAPIUID-Strukturen](mapiuid.md) im  _lpppUIDArray-Array,_ um die Empfängereintragsbezeichner zu identifizieren, die direkt vom Transportanbieter oder vom Messagingsystem verarbeitet werden, mit dem der Transportanbieter eine Verbindung herstellt. Weder MAPI noch der #A0 erweitern Adressen mithilfe von Eintragsbezeichnern, die in diesen **MAPIUID-Strukturen enthalten** sind. Diese Strukturen werden nur für die Empfängertypidentifikation verwendet. 
  
Der MAPI-Spooler verwendet jede zeichenfolge im  _lpppszAdrTypeArray-Parameter_ für einen Vergleichstest, wenn er entscheidet, welcher Transportanbieter welche Empfänger für eine ausgehende Nachricht verarbeiten soll. Wenn die PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft eines Nachrichtenempfängers exakt mit einer Zeichenfolge entspricht, die einen der vom Transportanbieter zur Verfügung stellten Messagingadressentypen identifiziert, kann der Anbieter die Nachricht an diesen Empfänger senden.
  
Wenn mehrere Transportanbieter denselben Empfängertyp verarbeiten können, wählt MAPI einen Transportanbieter basierend auf der Transportprioritätsreihenfolge aus, die im Profil der Clientanwendung angegeben ist. Um zu bestimmen, welcher Transportanbieter verwendet werden soll, überprüft der MAPI-Spooler alle vom Anbieter angegebenen **MAPIUID-Strukturen** in Prioritätsreihenfolge und anschließend alle vom Anbieter angegebenen Adresstypwerte in Prioritätsreihenfolge. Der erste Transportanbieter, der bei dieser Überprüfung mit einem bestimmten Empfänger übereinstimmen soll, erhält die erste Möglichkeit, diesen Empfänger zu verarbeiten. Wenn dieser Anbieter den Empfänger nicht verarbeitet, setzt der MAPI-Spooler die Überprüfung fort, um einen Transportanbieter für einen Empfänger zu finden, der noch nicht verarbeitet wurde. Die Überprüfung wird fortgesetzt, bis keine weiteren Übereinstimmungen gefunden wurden. An diesem Punkt wird für empfänger, die nicht verarbeitet wurden, ein Unauslöschungsbericht generiert. 
  
Wenn der Anbieter immer einen bestimmten Satz von Empfängertypen unterstützt, können der Adresstyp und **die MAPIUID-Arrays,** die der Transportanbieter übergeben hat, statisch sein. Wenn der Transportanbieter diese Arrays dynamisch erstellt, kann er Arbeitsspeicher mithilfe des Supportobjekts zuweisen, das zuvor im Aufruf von **TransportLogon** übergeben wurde, obwohl dies nicht erforderlich ist.
  
Der für den Adresstyp und die **MAPIUID-Arrays** verwendete Arbeitsspeicher sollte bis zum letzten Aufruf der [IXPLogon::TransportLogoff-Methode](ixplogon-transportlogoff.md) zugewiesen bleiben, zu dem der Transportanbieter den Arbeitsspeicher bei Bedarf frei geben kann. Der Transportanbieter sollte den Inhalt dieser Arrays nicht ändern, nachdem er vom **TransportLogoff-Aufruf zurückgegeben** wurde. 
  
Ein Transportanbieter, der jeden Empfängertyp verarbeiten kann, kann NULL im  _lpppszAdrTypeArray-Parameter_ zurückgeben. Transportanbieter für LAN-basierte Messagingsysteme, die einen zentralen Server verwenden, um ausgehende Nachrichten an verschiedene fremde Nachrichtensysteme zu senden, tun dies in der Regel. Dieser Transportanbietertyp sollte zuletzt in der Prioritätsreihenfolge der Transportanbieter im Profil der MAPI- und MAPI-Spooler installiert werden. 
  
Ein Transportanbieter, der ausgehende Nachrichten, die basierend auf dem Adresstyp an ihn gesendet werden, nicht unterstützt, sollte eine einzelne zeichenfolge ohne Länge in _lpppszAdrTypeArray zurückgeben._ Wenn ein Transportanbieter keine Empfängertypen unterstützt, sollte er NULL für die **MAPIUID-Struktur** und eine leere Zeichenfolge für den Adresstyp übergeben. Transportanbieter dieses Typs werden am häufigsten zum Installieren eines Nachrichtenvorprozessors verwendet. 
  
## <a name="see-also"></a>Siehe auch



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

