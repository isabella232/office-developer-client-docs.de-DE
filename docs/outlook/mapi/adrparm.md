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
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791290"
---
# <a name="adrparm"></a><span data-ttu-id="f90ee-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="f90ee-103">ADRPARM</span></span>

<span data-ttu-id="f90ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f90ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f90ee-105">Beschreibt die Anzeige und das Verhalten des Dialogfelds allgemeine Adresse.</span><span class="sxs-lookup"><span data-stu-id="f90ee-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f90ee-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f90ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="f90ee-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f90ee-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f90ee-108">Members</span><span class="sxs-lookup"><span data-stu-id="f90ee-108">Members</span></span>

<span data-ttu-id="f90ee-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="f90ee-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="f90ee-110">Anzahl der Bytes in die Eintrags-ID auf **LpABContEntryID**zeigt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="f90ee-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="f90ee-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="f90ee-112">Zeiger auf die Eintrags-ID des Containers, die die ursprüngliche Liste der Empfängeradressen bereitstellt, die im Dialogfeld Adresse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="f90ee-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f90ee-113">**ulFlags**</span></span>
  
> <span data-ttu-id="f90ee-114">Bitmaske aus Flags, die mit verschiedenen Adresse Dialogfeldoptionen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="f90ee-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f90ee-115">The following flags can be set:</span></span>
    
<span data-ttu-id="f90ee-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="f90ee-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="f90ee-117">Aktivieren Sie alle Namen aufgelöst werden, nachdem das Dialogfeld Adresse geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f90ee-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="f90ee-118">Wenn mehrdeutige Einträge, die aus der Namensauflösungsprozess vorhanden sind, wird ein Dialogfeld angezeigt, um den Benutzer für die Hilfe in Ihrer Lösung aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="f90ee-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="f90ee-119">Einstellung dieses Flag wird sichergestellt, dass alle [IAddrBook::Address](iaddrbook-address.md) zurückgegebenen Namen aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="f90ee-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="f90ee-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="f90ee-121">Deaktivieren Sie die Erstellung von einmal-Adressen für eine Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="f90ee-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="f90ee-122">Dieses Kennzeichen werden verwendet, nur, wenn das Dialogfeld modal, wird durch das DIALOG_MODAL-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="f90ee-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="f90ee-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="f90ee-124">Der Benutzer kann genau ein Empfänger anstatt mehrere Empfänger aus einer Liste auswählen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="f90ee-125">Dieses Kennzeichen gilt nur, wenn **cDestFields** 0 (null ist) und das Dialogfeld ist modal, durch das DIALOG_MODAL-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="f90ee-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f90ee-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f90ee-127">Bewirkt, dass die modale Version der Adresse im allgemeinen Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="f90ee-128">Entweder dieses Flag oder DIALOG_SDI sollte festgelegt werden. Sie können nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="f90ee-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="f90ee-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="f90ee-130">Bewirkt, dass die Schaltfläche **Optionen senden** , die im Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="f90ee-131">Dieses Kennzeichen werden verwendet, nur, wenn das Dialogfeld modal, wird durch das DIALOG_MODAL-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="f90ee-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f90ee-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f90ee-133">Bewirkt, dass die ohne Modus Version der Adresse im allgemeinen Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="f90ee-134">Entweder dieses Flag oder DIALOG_MODAL sollte festgelegt werden. Sie können nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="f90ee-135">Das Flag DIALOG_SDI für nicht-Outlook-Clients ignoriert, und die modale Version des Dialogfelds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="f90ee-136">Ein Zeiger auf ein Handle sollte daher nicht im _LpulUIParam_ -Parameter der [IAddrBook::Address](iaddrbook-address.md)erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="f90ee-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="f90ee-137">**lpReserved**</span></span>
  
> <span data-ttu-id="f90ee-138">Reserviert, muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f90ee-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="f90ee-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="f90ee-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="f90ee-140">Gibt den Kontext innerhalb **helfen** , die zuerst angezeigt werden, wenn der Benutzer auf die Schaltfläche Hilfe klicken Sie im Dialogfeld Adresse klickt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="f90ee-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="f90ee-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="f90ee-142">Zeiger auf den Namen einer Hilfedatei, die im Dialogfeld Adresse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="f90ee-143">Das Element **LpszHelpFileName** wird zusammen mit **UlHelpContext** aufrufen, die Windows- **WinHelp** -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="f90ee-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="f90ee-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="f90ee-145">Zeiger auf eine MAPI-Funktion basierend auf dem [ACCELERATEABSDI](accelerateabsdi.md) Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="f90ee-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="f90ee-146">Dieser Member gilt für die ohne Modus Version des Dialogfelds nur durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="f90ee-147">Erstellen eine **ADRPARM** -Struktur zum Übergeben an [IAddrBook::Address](iaddrbook-address.md) Clients müssen immer den **LpfnABSDI** Member auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="f90ee-148">Wenn das Flag DIALOG_SDI festgelegt ist, wird MAPI es auf eine gültige Funktion vor der Rückgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="f90ee-149">Clients rufen Sie diese Funktion aus in ihre Nachrichtenschleife hinzu, um sicherzustellen, dass in der Adresse Beschleuniger zum Dialogfeld Feld Arbeit Buch.</span><span class="sxs-lookup"><span data-stu-id="f90ee-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="f90ee-150">Wenn das Dialogfeld geschlossen und MAPI-Aufrufen der Funktion an, von dem **LpfnDismiss** Member auf, sollten Clients die Funktion **ACCELERATEABSDI** aus ihrer Nachrichtenschleife aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="f90ee-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="f90ee-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="f90ee-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="f90ee-152">Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL.</span><span class="sxs-lookup"><span data-stu-id="f90ee-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="f90ee-153">Dieser Member gilt nur für die ohne Modus Version des Dialogfelds nur durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="f90ee-154">MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse aufrufen **IAddrBook::Address** , dass das Dialogfeld nicht mehr aktiv ist Client darüber informieren.</span><span class="sxs-lookup"><span data-stu-id="f90ee-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="f90ee-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="f90ee-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="f90ee-156">Zeiger auf Kontextinformationen an die Funktion **DISMISSMODELESS** übergeben werden, auf dem **LpfnDismiss** Mitglied zeigt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="f90ee-157">Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="f90ee-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="f90ee-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="f90ee-159">Zeiger auf Text, der als Titel für das Dialogfeld allgemeine Adresse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="f90ee-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="f90ee-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="f90ee-161">Zeiger auf Text, der als Bezeichnung der Schaltfläche für die Schaltfläche verwendet werden, die im Dialogfeld **Neuen Eintrag** oder ein anderes Dialogfeld aufruft.</span><span class="sxs-lookup"><span data-stu-id="f90ee-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="f90ee-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="f90ee-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="f90ee-163">Zeiger auf Text, der als Titel für die Empfänger Textfeld-Steuerelemente verwendet werden, die in der modal Version im Dialogfeld allgemeine Adresse angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="f90ee-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="f90ee-164">Dieser Member ist nicht für nicht modale Dialogfelder verwendet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="f90ee-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="f90ee-165">**cDestFields**</span></span>
  
> <span data-ttu-id="f90ee-166">Anzahl der Empfänger Textfeld-Steuerelemente in der modal Version von im Dialogfeld Adresse oder NULL, wenn das Dialogfeld ohne Modus ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="f90ee-167">Das Dialogfeld Adresse wird geöffnet, zum Durchsuchen von nur, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="f90ee-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="f90ee-168">Das **cDestFields** -Element wird auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="f90ee-169">Das Flag DIALOG_BOX festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="f90ee-170">Das Flag ADDRESS_ONE ist nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="f90ee-171">Festlegen von **cDestFields** auf 0XFFFFFFFF impliziert, dass die Standardanzahl zulässiger Empfänger Text von MAPI-Steuerelemente erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f90ee-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="f90ee-172">In diesem Fall müssen die Member **LppszDestTitles** und **LpulDestComps** NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f90ee-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="f90ee-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="f90ee-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="f90ee-174">Gibt an, das bestimmten Textfeld-Steuerelement, das das Hauptaugenmerk verfügen soll, wenn die modale Version des Dialogfelds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f90ee-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="f90ee-175">Dieser Wert muss zwischen 0 und der Wert der **cDestFields** minus 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="f90ee-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="f90ee-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="f90ee-177">Zeiger auf ein Array von Beschriftungen für die Schaltflächen mit den einzelnen Textfeld-Steuerelemente, die in der modal Version des Dialogfelds Adresse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="f90ee-178">Der Wert des Elements **cDestFields** gibt die Anzahl der Etiketten, die in das Array aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="f90ee-179">Wenn der **LppszDestTitles** Member NULL ist, wird die **Adresse** -Methode Standard Titel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="f90ee-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="f90ee-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="f90ee-181">Zeiger auf ein Array von Werten Empfängertyp, wie MAPI_TO, MAPI_CC und MAPI_BCC, jedes Textfeld-Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="f90ee-182">Der Wert des Elements **CDestFields** gibt die Anzahl von Empfängertypen in das Array aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="f90ee-183">Die Werte auf die **LpulDestComps** können verwendet werden, die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))-Eigenschaft der einzelnen Empfänger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="f90ee-184">Wenn der **LpulDestComps** Member NULL ist, wird die **Adresse** -Methode Empfängertypen Standard verwendet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="f90ee-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="f90ee-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="f90ee-186">Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die den Typ der Adresseinträge beschränkt, die im Dialogfeld angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f90ee-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="f90ee-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="f90ee-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="f90ee-188">Zeiger auf eine **SRestriction** -Struktur, die die Address Book Container beschränkt, die Adresseinträge im Dialogfeld anzuzeigende bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="f90ee-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f90ee-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f90ee-189">Remarks</span></span>

<span data-ttu-id="f90ee-190">**ADRPARM** Strukturen werden von Clients und -Dienstanbieter verwendet, um das Aussehen und Verhalten der MAPI-allgemeine Adresse Dialogfelder zu steuern.</span><span class="sxs-lookup"><span data-stu-id="f90ee-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="f90ee-191">Es gibt zwei Arten des Dialogfelds Adresse: ohne Modus und modal.</span><span class="sxs-lookup"><span data-stu-id="f90ee-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="f90ee-192">Einige der Elemente in der Struktur **ADRPARM** gelten für beide Versionen des Dialogfelds, aber einige gelten nur für eine der beiden Versionen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="f90ee-193">In der folgenden Tabelle betrifft die Mitglieder einer **ADRPARM** Struktur für ihre Verwendung mit der Standarddialogfelder Adresse.</span><span class="sxs-lookup"><span data-stu-id="f90ee-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="f90ee-194">ADRPARM member</span><span class="sxs-lookup"><span data-stu-id="f90ee-194">ADRPARM member</span></span>|<span data-ttu-id="f90ee-195">Typ des Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="f90ee-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="f90ee-196">**CbABContEntryID** und **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="f90ee-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="f90ee-197">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f90ee-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="f90ee-199">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="f90ee-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="f90ee-201">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-202">**UlHelpContext** und **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="f90ee-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="f90ee-203">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="f90ee-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="f90ee-205">Ungebunden</span><span class="sxs-lookup"><span data-stu-id="f90ee-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-206">**LpfnDismiss** und **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="f90ee-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="f90ee-207">Ungebunden</span><span class="sxs-lookup"><span data-stu-id="f90ee-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="f90ee-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="f90ee-209">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="f90ee-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="f90ee-211">Modales</span><span class="sxs-lookup"><span data-stu-id="f90ee-211">Modal</span></span>  <br/> |
|<span data-ttu-id="f90ee-212">**LpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **LppszDestTitles**und **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="f90ee-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="f90ee-213">Modales</span><span class="sxs-lookup"><span data-stu-id="f90ee-213">Modal</span></span>  <br/> |
|<span data-ttu-id="f90ee-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="f90ee-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="f90ee-215">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="f90ee-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="f90ee-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="f90ee-217">Modale und nicht modale</span><span class="sxs-lookup"><span data-stu-id="f90ee-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="f90ee-218">Das Dialogfeld ohne Modus ist eine schreibgeschützte Darstellung von Einträgen aus einen oder mehrere Address Book Container.</span><span class="sxs-lookup"><span data-stu-id="f90ee-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="f90ee-219">Das Dialogfeld kann alle Einträge aus der ausgewählten Container ein- oder auf begrenzt nur die Einträge und Containern, die durch eine Einschränkung festgelegten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="f90ee-220">Die Einschränkung der Inhalt auf den **LpContRestriction** kann die Typen der angezeigten Einträge beschränkt, und die Einschränkung der Hierarchie auf den **LpHierRestriction** kann die Container bereitstellen die Einträge beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="f90ee-221">Um den Anrufer informieren, wann das Dialogfeld geschlossen wird, ruft MAPI eine Funktion, die vom Anrufer bereitgestellt wird, die den [DISMISSMODELESS](dismissmodeless.md) Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="f90ee-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="f90ee-222">Eine andere Funktion, mit den Prototyp [ACCELERATEABSDI](accelerateabsdi.md) übereinstimmt MAPI bereitgestellt und aufgerufen, die vom Anrufer in der Windows-Nachrichtenschleife in das Funktionieren der Tastenkombinationen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="f90ee-223">Die ohne Modus Version des Dialogfelds MAPI-Adresse kann angezeigt werden, wenn Clients [IAddrBook::Address](iaddrbook-address.md) aufrufen oder Dienstanbieter [IMAPISupport::Address](imapisupport-address.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f90ee-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="f90ee-224">Das modale Dialogfeld ist eine Lese-Schreib-Darstellung der Einträge aus mindestens einen Container.</span><span class="sxs-lookup"><span data-stu-id="f90ee-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="f90ee-225">Seinen Inhalt können auf die gleiche Weise betroffen sein, wie in den **LpContRestriction** und **LpHierRestriction** Mitglieder die ohne Modus Version von Einschränkungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="f90ee-226">Zusätzlich zur Anzeige der Container Einträge im Listenfeld kann das modale Dialogfeld zwischen einem und drei Textfeld-Steuerelemente zum Aufbewahren von vom Benutzer ausgewählten Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="f90ee-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="f90ee-227">Jedes Bearbeitungssteuerelement ist einer bestimmten Empfängertyp oder **PR_RECIPIENT_TYPE** -Eigenschaft, wie etwa MAPI_TO zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="f90ee-228">Modales Dialogfeld Adressfeld kann mithilfe der Methoden **Adresse** oder angezeigt werden, wenn Clients [IAddrBook::Details](iaddrbook-details.md) -Dienstanbieter aufrufen und [IMAPISupport::Details](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="f90ee-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="f90ee-229">Die folgende Abbildung enthält zwei Textfeld-Steuerelemente, da das **cDestFields** Mitglied der **ADRPARM** -Struktur, die Steuerung der Anzeige dieses Dialogfelds auf 2 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="f90ee-230">Das erste Steuerelement hat Hauptaugenmerk, da das Element **nDestFieldFocus** auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f90ee-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="f90ee-231">**LpszNewEntryTitle** Member verweist auf eine Schaltfläche Beschriftungstext, die, wenn er ausgewählt ist, wird ein weiteres Dialogfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f90ee-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="f90ee-232">In der Regel wie in der Abbildung im modalen Dialogfeld angezeigt wird, ist die Schaltfläche **neu** gekennzeichnet, und klicken Sie im Dialogfeld listet alle Typen von Adressen, die erstellt werden können von jedem der adressbuchanbietern implementierte im Profil.</span><span class="sxs-lookup"><span data-stu-id="f90ee-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="f90ee-233">Clients führen dazu, dass das Dialogfeld **Neuen Eintrag** , durch Aufrufen von [IAddrBook::NewEntry](iaddrbook-newentry.md) und 0 (null) für den Parameter _CbEidNewEntryTpl_ und NULL für den Parameter _LpEidNewEntryTpl_ übergeben, wenn der Benutzer die Schaltfläche auswählt angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f90ee-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="f90ee-234">Die Informationen, die in diesem Dialogfeld enthalten ist, stammen aus der einmaligen MAPI-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f90ee-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="f90ee-235">Jeder Eintrag in diesem Dialogfeld ist eine Vorlage für die Dateneingabe erforderlich, um eine Adresse eines bestimmten Typs erstellen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f90ee-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="f90ee-236">Die meisten adressbuchanbietern implementierte Geben Sie eine Vorlage für jede Art von Adresseintrag, die sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="f90ee-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="f90ee-237">Wenn ein Benutzer in diesem Dialogfeld eine Auswahl treffen, zeigt MAPI die entsprechende Vorlage.</span><span class="sxs-lookup"><span data-stu-id="f90ee-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="f90ee-238">Die vier wichtigsten Bits die **ADRPARM** Struktur **UlFlags** Members enthalten eine Versionsnummer, die die Version der Struktur **ADRPARM** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f90ee-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="f90ee-239">Die aktuelle Version ist 0 (null) oder ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="f90ee-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="f90ee-240">Die aktuelle Implementierung von MAPI schlägt fehl, für alle Versionen der Struktur als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f90ee-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="f90ee-241">Zukünftige Versionen der Struktur möglicherweise ganz anderen; Sie können die Version-NULL-Struktur nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f90ee-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="f90ee-242">Die folgenden Makros werden zum Extrahieren der Versionsnummer aus der **UlFlags** Member und für die Kombination mit den definierten Flags bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="f90ee-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="f90ee-243">**GET_ADRPARM_VERSION** (_UlFlags_)</span><span class="sxs-lookup"><span data-stu-id="f90ee-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="f90ee-244">**SET_ADRPARM_VERSION** (_UlFlags_, _ UlVersion _)</span><span class="sxs-lookup"><span data-stu-id="f90ee-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="f90ee-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="f90ee-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f90ee-246">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f90ee-246">See also</span></span>

- [<span data-ttu-id="f90ee-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="f90ee-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="f90ee-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="f90ee-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="f90ee-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="f90ee-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="f90ee-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="f90ee-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="f90ee-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="f90ee-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="f90ee-252">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f90ee-252">MAPI Structures</span></span>](mapi-structures.md)

