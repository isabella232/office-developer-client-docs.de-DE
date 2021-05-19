---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420374"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion zum Verarbeiten von Zugriffstasten in einem Dialogfeld ohne Adressbuch. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion, die von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Anwendungen, die unter Microsoft Windows ausgeführt werden, ist _ulUIParam_ das übergeordnete Fensterhandle für ein Dialogfeld und hat den Typ HWND, wird in ein ULONG_PTR **.** Der Wert Null gibt an, dass kein übergeordnetes Fenster besteht. 
    
 _lpvmsg_
  
> [in] Zeiger auf eine Windows Nachricht.
    
## <a name="return-value"></a>Rückgabewert

Eine Funktion mit dem **ACCELERATEABSDI-Prototyp** gibt TRUE zurück, wenn sie die Nachricht verarbeitet. 
  
## <a name="remarks"></a>Hinweise

Eine auf dem **ACCELERATEABSDI-Prototyp** basierende Funktion wird nur mit einem moduslosen Dialogfeld verwendet, d. h. nur, wenn die Clientanwendung das flag DIALOG_SDI im  _ulFlags-Element_ der [ADRPARM-Struktur](adrparm.md) festgelegt hat. 
  
Ein modusloses Dialogfeld gibt die Nachrichtenschleife der Clientanwendung Windows, anstatt eine eigene Schleife zu haben. Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht, welche Zugriffstasten das Dialogfeld verwendet. Daher wird eine **ACCELERATEABSDI-basierte** Funktion aufgerufen, um Tastenkombinationen wie STRG+P zum Drucken zu testen und diese zu verwenden. 
  
Die Nachrichtenschleife eines Clients ruft die **ACCELERATEABSDI-basierte** Funktion auf, wenn der Client ein Dialogfeld ohne Adressbuch mit der [IAddrBook::Address-Methode](iaddrbook-address.md) aufruft. Dieser Aufruf wird beendet, wenn MAPI eine Funktion aufruft, die auf dem [PROTOTYP der DISMISSMODELESS-Funktion](dismissmodeless.md) basiert. 
  

