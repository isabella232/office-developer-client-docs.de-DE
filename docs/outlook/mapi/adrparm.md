---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ad26cb9b77404d6470f7a8d787eb85edc5cce402
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19791290"
---
# <a name="adrparm"></a>ADRPARM

**Betrifft**: Outlook 
  
Beschreibt die Anzeige und das Verhalten des Dialogfelds allgemeine Adresse. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Anzahl der Bytes in die Eintrags-ID auf **LpABContEntryID**zeigt.
    
**lpABContEntryID**
  
> Zeiger auf die Eintrags-ID des Containers, die die ursprüngliche Liste der Empfängeradressen bereitstellt, die im Dialogfeld Adresse angezeigt werden.
    
**ulFlags**
  
> Bitmaske aus Flags, die mit verschiedenen Adresse Dialogfeldoptionen verknüpft ist. Die folgenden Kennzeichen können festgelegt werden:
    
AB_RESOLVE
  
> Aktivieren Sie alle Namen aufgelöst werden, nachdem das Dialogfeld Adresse geschlossen wurde. Wenn mehrdeutige Einträge, die aus der Namensauflösungsprozess vorhanden sind, wird ein Dialogfeld angezeigt, um den Benutzer für die Hilfe in Ihrer Lösung aufzufordern. Einstellung dieses Flag wird sichergestellt, dass alle [IAddrBook::Address](iaddrbook-address.md) zurückgegebenen Namen aufgelöst werden. 
    
AB_SELECTONLY
  
> Deaktivieren Sie die Erstellung von einmal-Adressen für eine Empfängerliste. Dieses Kennzeichen werden verwendet, nur, wenn das Dialogfeld modal, wird durch das DIALOG_MODAL-Flag festgelegt wird.
    
ADDRESS_ONE
  
> Der Benutzer kann genau ein Empfänger anstatt mehrere Empfänger aus einer Liste auswählen. Dieses Kennzeichen gilt nur, wenn **cDestFields** 0 (null ist) und das Dialogfeld ist modal, durch das DIALOG_MODAL-Flag festgelegt wird. 
    
DIALOG_MODAL
  
> Bewirkt, dass die modale Version der Adresse im allgemeinen Dialogfeld angezeigt werden. Entweder dieses Flag oder DIALOG_SDI sollte festgelegt werden. Sie können nicht festgelegt werden. 
    
DIALOG_OPTIONS
  
> Bewirkt, dass die Schaltfläche **Optionen senden** , die im Dialogfeld angezeigt werden. Dieses Kennzeichen werden verwendet, nur, wenn das Dialogfeld modal, wird durch das DIALOG_MODAL-Flag festgelegt wird. 
    
DIALOG_SDI
  
> Bewirkt, dass die ohne Modus Version der Adresse im allgemeinen Dialogfeld angezeigt werden. Entweder dieses Flag oder DIALOG_MODAL sollte festgelegt werden. Sie können nicht festgelegt werden. Das Flag DIALOG_SDI für nicht-Outlook-Clients ignoriert, und die modale Version des Dialogfelds angezeigt. Ein Zeiger auf ein Handle sollte daher nicht im _LpulUIParam_ -Parameter der [IAddrBook::Address](iaddrbook-address.md)erwartet werden.
    
**lpReserved**
  
> Reserviert, muss NULL sein.
    
**ulHelpContext**
  
> Gibt den Kontext innerhalb **helfen** , die zuerst angezeigt werden, wenn der Benutzer auf die Schaltfläche Hilfe klicken Sie im Dialogfeld Adresse klickt. 
    
**lpszHelpFileName**
  
> Zeiger auf den Namen einer Hilfedatei, die im Dialogfeld Adresse zugeordnet werden. Das Element **LpszHelpFileName** wird zusammen mit **UlHelpContext** aufrufen, die Windows- **WinHelp** -Funktion verwendet. 
    
**lpfnABSDI**
  
> Zeiger auf eine MAPI-Funktion basierend auf dem [ACCELERATEABSDI](accelerateabsdi.md) Prototyp oder NULL. Dieser Member gilt für die ohne Modus Version des Dialogfelds nur durch das DIALOG_SDI-Flag festgelegt wird. Erstellen eine **ADRPARM** -Struktur zum Übergeben an [IAddrBook::Address](iaddrbook-address.md) Clients müssen immer den **LpfnABSDI** Member auf NULL festgelegt. Wenn das Flag DIALOG_SDI festgelegt ist, wird MAPI es auf eine gültige Funktion vor der Rückgabe festgelegt. Clients rufen Sie diese Funktion aus in ihre Nachrichtenschleife hinzu, um sicherzustellen, dass in der Adresse Beschleuniger zum Dialogfeld Feld Arbeit Buch. Wenn das Dialogfeld geschlossen und MAPI-Aufrufen der Funktion an, von dem **LpfnDismiss** Member auf, sollten Clients die Funktion **ACCELERATEABSDI** aus ihrer Nachrichtenschleife aufzuheben. 
    
**lpfnDismiss**
  
> Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL. Dieser Member gilt nur für die ohne Modus Version des Dialogfelds nur durch das DIALOG_SDI-Flag festgelegt wird. MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse aufrufen **IAddrBook::Address** , dass das Dialogfeld nicht mehr aktiv ist Client darüber informieren. 
    
**lpvDismissContext**
  
> Zeiger auf Kontextinformationen an die Funktion **DISMISSMODELESS** übergeben werden, auf dem **LpfnDismiss** Mitglied zeigt. Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird. 
    
**lpszCaption**
  
> Zeiger auf Text, der als Titel für das Dialogfeld allgemeine Adresse verwendet werden.
    
**lpszNewEntryTitle**
  
> Zeiger auf Text, der als Bezeichnung der Schaltfläche für die Schaltfläche verwendet werden, die im Dialogfeld **Neuen Eintrag** oder ein anderes Dialogfeld aufruft. 
    
**lpszDestWellsTitle**
  
> Zeiger auf Text, der als Titel für die Empfänger Textfeld-Steuerelemente verwendet werden, die in der modal Version im Dialogfeld allgemeine Adresse angezeigt werden können. Dieser Member ist nicht für nicht modale Dialogfelder verwendet. 
    
**cDestFields**
  
> Anzahl der Empfänger Textfeld-Steuerelemente in der modal Version von im Dialogfeld Adresse oder NULL, wenn das Dialogfeld ohne Modus ist. Das Dialogfeld Adresse wird geöffnet, zum Durchsuchen von nur, wenn Folgendes zutrifft: 
    
  - Das **cDestFields** -Element wird auf 0 (null) festgelegt. 
    
  - Das Flag DIALOG_BOX festgelegt ist.
    
  - Das Flag ADDRESS_ONE ist nicht festgelegt.
    
  Festlegen von **cDestFields** auf 0XFFFFFFFF impliziert, dass die Standardanzahl zulässiger Empfänger Text von MAPI-Steuerelemente erstellt werden soll. In diesem Fall müssen die Member **LppszDestTitles** und **LpulDestComps** NULL sein. 
    
**nDestFieldFocus**
  
> Gibt an, das bestimmten Textfeld-Steuerelement, das das Hauptaugenmerk verfügen soll, wenn die modale Version des Dialogfelds angezeigt wird. Dieser Wert muss zwischen 0 und der Wert der **cDestFields** minus 1 liegen. 
    
**lppszDestTitles**
  
> Zeiger auf ein Array von Beschriftungen für die Schaltflächen mit den einzelnen Textfeld-Steuerelemente, die in der modal Version des Dialogfelds Adresse angezeigt werden. Der Wert des Elements **cDestFields** gibt die Anzahl der Etiketten, die in das Array aufgenommen. Wenn der **LppszDestTitles** Member NULL ist, wird die **Adresse** -Methode Standard Titel verwendet. 
    
**lpulDestComps**
  
> Zeiger auf ein Array von Werten Empfängertyp, wie MAPI_TO, MAPI_CC und MAPI_BCC, jedes Textfeld-Steuerelement zugeordnet ist. Der Wert des Elements **CDestFields** gibt die Anzahl von Empfängertypen in das Array aufgenommen. Die Werte auf die **LpulDestComps** können verwendet werden, die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft der einzelnen Empfänger festgelegt. Wenn der **LpulDestComps** Member NULL ist, wird die **Adresse** -Methode Empfängertypen Standard verwendet. 
    
**lpContRestriction**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die den Typ der Adresseinträge beschränkt, die im Dialogfeld angezeigt werden kann. 
    
**lpHierRestriction**
  
> Zeiger auf eine **SRestriction** -Struktur, die die Address Book Container beschränkt, die Adresseinträge im Dialogfeld anzuzeigende bereitstellen können. 
    
## <a name="remarks"></a>Hinweise

**ADRPARM** Strukturen werden von Clients und -Dienstanbieter verwendet, um das Aussehen und Verhalten der MAPI-allgemeine Adresse Dialogfelder zu steuern. Es gibt zwei Arten des Dialogfelds Adresse: ohne Modus und modal. Einige der Elemente in der Struktur **ADRPARM** gelten für beide Versionen des Dialogfelds, aber einige gelten nur für eine der beiden Versionen. In der folgenden Tabelle betrifft die Mitglieder einer **ADRPARM** Struktur für ihre Verwendung mit der Standarddialogfelder Adresse. 
  
|ADRPARM member|Typ des Dialogfelds|
|:-----|:-----|
|**CbABContEntryID** und **lpABContEntryID** <br/> |Modale und nicht modale  <br/> |
|**ulFlags** <br/> |Modale und nicht modale  <br/> |
|**lpReserved** <br/> |Modale und nicht modale  <br/> |
|**UlHelpContext** und **lpszHelpFileName** <br/> |Modale und nicht modale  <br/> |
|**lpfnABSDI** <br/> |Ungebunden  <br/> |
|**LpfnDismiss** und **lpvDismissContext** <br/> |Ungebunden  <br/> |
|**lpszCaption** <br/> |Modale und nicht modale  <br/> |
|**lpszNewEntryTitle** <br/> |Modales  <br/> |
|**LpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **LppszDestTitles**und **lpulDestComps** <br/> |Modales  <br/> |
|**lpContRestriction** <br/> |Modale und nicht modale  <br/> |
|**lpHierRestriction** <br/> |Modale und nicht modale  <br/> |
   
Das Dialogfeld ohne Modus ist eine schreibgeschützte Darstellung von Einträgen aus einen oder mehrere Address Book Container. Das Dialogfeld kann alle Einträge aus der ausgewählten Container ein- oder auf begrenzt nur die Einträge und Containern, die durch eine Einschränkung festgelegten Kriterien entsprechen. Die Einschränkung der Inhalt auf den **LpContRestriction** kann die Typen der angezeigten Einträge beschränkt, und die Einschränkung der Hierarchie auf den **LpHierRestriction** kann die Container bereitstellen die Einträge beschränkt. Um den Anrufer informieren, wann das Dialogfeld geschlossen wird, ruft MAPI eine Funktion, die vom Anrufer bereitgestellt wird, die den [DISMISSMODELESS](dismissmodeless.md) Prototyp entspricht. Eine andere Funktion, mit den Prototyp [ACCELERATEABSDI](accelerateabsdi.md) übereinstimmt MAPI bereitgestellt und aufgerufen, die vom Anrufer in der Windows-Nachrichtenschleife in das Funktionieren der Tastenkombinationen zu vereinfachen. Die ohne Modus Version des Dialogfelds MAPI-Adresse kann angezeigt werden, wenn Clients [IAddrBook::Address](iaddrbook-address.md) aufrufen oder Dienstanbieter [IMAPISupport::Address](imapisupport-address.md)aufgerufen. 
  
Das modale Dialogfeld ist eine Lese-Schreib-Darstellung der Einträge aus mindestens einen Container. Seinen Inhalt können auf die gleiche Weise betroffen sein, wie in den **LpContRestriction** und **LpHierRestriction** Mitglieder die ohne Modus Version von Einschränkungen festgelegt. Zusätzlich zur Anzeige der Container Einträge im Listenfeld kann das modale Dialogfeld zwischen einem und drei Textfeld-Steuerelemente zum Aufbewahren von vom Benutzer ausgewählten Einträge enthalten. Jedes Bearbeitungssteuerelement ist einer bestimmten Empfängertyp oder **PR_RECIPIENT_TYPE** -Eigenschaft, wie etwa MAPI_TO zugeordnet. Modales Dialogfeld Adressfeld kann mithilfe der Methoden **Adresse** oder angezeigt werden, wenn Clients [IAddrBook::Details](iaddrbook-details.md) -Dienstanbieter aufrufen und [IMAPISupport::Details](imapisupport-details.md). 
  
Die folgende Abbildung enthält zwei Textfeld-Steuerelemente, da das **cDestFields** Mitglied der **ADRPARM** -Struktur, die Steuerung der Anzeige dieses Dialogfelds auf 2 festgelegt ist. Das erste Steuerelement hat Hauptaugenmerk, da das Element **nDestFieldFocus** auf 0 festgelegt ist. 
  
**LpszNewEntryTitle** Member verweist auf eine Schaltfläche Beschriftungstext, die, wenn er ausgewählt ist, wird ein weiteres Dialogfeld angezeigt werden. In der Regel wie in der Abbildung im modalen Dialogfeld angezeigt wird, ist die Schaltfläche **neu** gekennzeichnet, und klicken Sie im Dialogfeld listet alle Typen von Adressen, die erstellt werden können von jedem der adressbuchanbietern implementierte im Profil. Clients führen dazu, dass das Dialogfeld **Neuen Eintrag** , durch Aufrufen von [IAddrBook::NewEntry](iaddrbook-newentry.md) und 0 (null) für den Parameter _CbEidNewEntryTpl_ und NULL für den Parameter _LpEidNewEntryTpl_ übergeben, wenn der Benutzer die Schaltfläche auswählt angezeigt werden soll. Die Informationen, die in diesem Dialogfeld enthalten ist, stammen aus der einmaligen MAPI-Tabelle. 
  
Jeder Eintrag in diesem Dialogfeld ist eine Vorlage für die Dateneingabe erforderlich, um eine Adresse eines bestimmten Typs erstellen zugeordnet. Die meisten adressbuchanbietern implementierte Geben Sie eine Vorlage für jede Art von Adresseintrag, die sie erstellen können. Wenn ein Benutzer in diesem Dialogfeld eine Auswahl treffen, zeigt MAPI die entsprechende Vorlage.
  
Die vier wichtigsten Bits die **ADRPARM** Struktur **UlFlags** Members enthalten eine Versionsnummer, die die Version der Struktur **ADRPARM** identifiziert. Die aktuelle Version ist 0 (null) oder ADRPARM_HELP_CTX. Die aktuelle Implementierung von MAPI schlägt fehl, für alle Versionen der Struktur als 0 (null). 
  
Zukünftige Versionen der Struktur möglicherweise ganz anderen; Sie können die Version-NULL-Struktur nicht unterstützt. Die folgenden Makros werden zum Extrahieren der Versionsnummer aus der **UlFlags** Member und für die Kombination mit den definierten Flags bereitgestellt: 
  
- **GET_ADRPARM_VERSION** (_UlFlags_) 
- **SET_ADRPARM_VERSION** (_UlFlags_, _ UlVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Siehe auch

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

