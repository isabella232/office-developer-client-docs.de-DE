---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5d291d49e07112082e5bf36c774fb0c687ea1f4b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592637"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion zum Verarbeiten von Tastenkombinationen in einem Dialogfeld ohne Adressbuch ohne Modus. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Anwendungen, die auf Microsoft Windows ausgeführt werden, ist _ulUIParam_ das übergeordnete Fensterhandle für ein Dialogfeld und hat den Typ HWND und wird in eine **ULONG_PTR** umgewandelt. Der Wert Null gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvmsg_
  
> [in] Zeiger auf eine Windows Nachricht.
    
## <a name="return-value"></a>Rückgabewert

Eine Funktion mit dem **ACCELERATEABSDI-Prototyp** gibt TRUE zurück, wenn sie die Nachricht verarbeitet. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Funktion, die auf dem **ACCELERATEABSDI-Prototyp** basiert, wird nur mit einem dialogfeld ohne Modus verwendet, d. h. nur, wenn die Clientanwendung das Flag DIALOG_SDI im  _ulFlags-Element_ der [ADRPARM-Struktur](adrparm.md) festgelegt hat. 
  
In einem dialogfeld ohne Modus wird die Windows Nachrichtenschleife der Clientanwendung verwendet, anstatt über eine eigene Schleife zu verfügen. Die Anwendung, die die Meldungsschleife steuert, weiß nicht, welche Tastenkombinationen das Dialogfeld verwendet. Daher wird eine **ACCELERATEABSDI-basierte** Funktion aufgerufen, um tastenkombinationen wie STRG+P zum Drucken zu testen und darauf zu reagieren. 
  
Die Nachrichtenschleife eines Clients ruft die **AUF ACCELERATEABSDI** basierende Funktion auf, wenn der Client ein Dialogfeld ohne Modus mit der [IAddrBook::Address-Methode](iaddrbook-address.md) aufruft. Dieser Aufruf wird beendet, wenn MAPI eine Funktion aufruft, die auf dem PROTOTYP der [DISMISSMODELESS-Funktion](dismissmodeless.md) basiert. 
  

