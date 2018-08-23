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
ms.openlocfilehash: 101e74f3e35e3664dd29e59f166b2f0af6e1dcba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592038"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Funktion basierend auf den **ACCELERATEABSDI** Prototyp ist nur mit einem modalen Dialogfeld, d. h., nur verwendet, wenn die Clientanwendung das Flag DIALOG_SDI im _UlFlags_ -Member der [ADRPARM](adrparm.md) -Struktur eingerichtet hat. 
  
Nicht modales Dialogfeld teilt die Clientanwendung Windows Nachrichtenschleife, anstatt einen eigenen Schleife. Die Anwendung, die die Nachrichtenschleife steuert, weiß nicht welche Zugriffstasten der Dialogfeld verwendet, damit es ein **ACCELERATEABSDI** aufruft, Grundlage Zugriffstasten wie STRG + P für den Druck Funktion zum Testen und fungieren. 
  
Ein Client Nachricht Schleife Aufrufe der **ACCELERATEABSDI** basierend Funktion, wenn der Client einen nicht modalen Adressbücher in Dialogfeldern mit der [IAddrBook::Address](iaddrbook-address.md) -Methode aufruft. In diesem Anruf wird beendet, wenn MAPI eine Funktion basierend auf den Prototyp [DISMISSMODELESS](dismissmodeless.md) -Funktion aufruft. 
  

