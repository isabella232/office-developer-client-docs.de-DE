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
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791247"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Betrifft**: Outlook 
  
Definiert eine Callback-Funktion zum Prozess Zugriffstasten in ein Dialogfeld ohne Modus Address Book. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |MAPI  <br/> |
|Definierte Funktion aufgerufen:  <br/> |Clientanwendungen  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Einen implementierungsspezifischen Wert für die Übergabe von Informationen zur Benutzeroberfläche auf eine Funktion verwendet. In Clientanwendungen unter Microsoft Windows _UlUIParam_ ist das übergeordnete Fensterhandle für ein Dialogfeld und vom Typ HWND in eine **ULONG_PTR**umgewandelt. Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvmsg_
  
> [in] Zeiger auf eine Windows-Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

Eine Funktion mit dem Prototyp **ACCELERATEABSDI** gibt TRUE zurück, wenn die Meldung behandelt. 
  
## <a name="remarks"></a>Hinweise

Eine Funktion basierend auf den **ACCELERATEABSDI** Prototyp ist nur mit einem modalen Dialogfeld, d. h., nur verwendet, wenn die Clientanwendung das Flag DIALOG_SDI im _UlFlags_ -Member der [ADRPARM](adrparm.md) -Struktur eingerichtet hat. 
  
Nicht modales Dialogfeld teilt die Clientanwendung Windows Nachrichtenschleife, anstatt einen eigenen Schleife. Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht welche Zugriffstasten der Dialogfeld verwendet, damit es ein **ACCELERATEABSDI** aufruft, Grundlage Zugriffstasten wie STRG + P für den Druck Funktion zum Testen und fungieren. 
  
Ein Client Nachricht Schleife Aufrufe der **ACCELERATEABSDI** basierend Funktion, wenn der Client einen nicht modalen Adressbücher in Dialogfeldern mit der [IAddrBook::Address](iaddrbook-address.md) -Methode aufruft. In diesem Anruf wird beendet, wenn MAPI eine Funktion basierend auf den Prototyp [DISMISSMODELESS](dismissmodeless.md) -Funktion aufruft. 
  

