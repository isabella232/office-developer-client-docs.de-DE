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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322127"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion zum Verarbeiten von Zugriffstasten in einem nicht modalen Adressbuch Dialogfeld. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Anwendungen, die unter Microsoft Windows laufen, ist _ulUIParam_ das übergeordnete Fensterhandle für ein Dialogfeld und vom Typ HWND und wird in eine **ULONG_PTR**umgewandelt. Der Wert 0 (null) gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvmsg_
  
> in Zeiger auf eine Windows-Nachricht.
    
## <a name="return-value"></a>Rückgabewert

Eine Funktion mit dem **ACCELERATEABSDI** -Prototyp gibt true zurück, wenn Sie die Nachricht verarbeitet. 
  
## <a name="remarks"></a>Bemerkungen

Eine auf dem **ACCELERATEABSDI** -Prototyp basierende Funktion wird nur mit einem nicht modalen Dialogfeldverwendet, das heißt nur, wenn die Clientanwendung das DIALOG_SDI-Flag im _ulFlags_ -Element der [ADRPARM](adrparm.md) -Struktur festgelegt hat. 
  
Ein nicht modales Dialogfeld teilt die Windows-Meldungsschleife der Clientanwendung, statt eine eigene Schleife zu haben. Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht, welche Tastenkombinationen im Dialogfeldverwendet werden, und ruft daher eine **ACCELERATEABSDI** -basierte Funktion auf, um Zugriffstasten wie STRG + P zum Drucken zu testen und zu reagieren. 
  
Die Meldungsschleife eines Clients Ruft die **ACCELERATEABSDI** -basierte Funktion auf, wenn der Client ein nicht modales Adressbuch-Dialogfeld mit der [IAddrBook:: Address](iaddrbook-address.md) -Methode aufruft. Dieser Aufruf wird beendet, wenn MAPI eine Funktion aufruft, die auf dem Prototyp der [DISMISSMODELESS](dismissmodeless.md) -Funktion basiert. 
  

