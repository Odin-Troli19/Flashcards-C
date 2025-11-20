# ❓ Frequently Asked Questions (FAQ)

Quick answers to common questions about Flashcard Master Pro.

## 📥 Installation & Setup

### Q: How do I install the app?
**A:** You don't need to install anything! Just download the `flashcard-app-indexeddb.html` file and open it in your web browser. That's it!

### Q: What browsers are supported?
**A:** Any modern browser:
- ✅ Chrome/Edge (version 24+)
- ✅ Firefox (version 16+)
- ✅ Safari (version 10+)
- ✅ Opera (version 15+)

### Q: Do I need an internet connection?
**A:** No! The app works 100% offline after you open it the first time. All data is stored on your computer.

### Q: Can I use it on my phone or tablet?
**A:** Yes! The app is fully responsive and works on mobile browsers. However, mobile browsers may have stricter storage limits (~50MB-500MB instead of unlimited).

---

## 💾 Data & Storage

### Q: Where is my data stored?
**A:** All your data is stored locally in your browser's IndexedDB. Nothing is sent to any server or cloud.

### Q: How much can I store?
**A:** With IndexedDB, you can store approximately 50-60% of your available disk space. If you have 100GB free, you can store ~50GB of flashcards!

### Q: What happens if I clear my browser data?
**A:** You'll lose all your flashcards! Always keep backups by exporting your data regularly (go to Backup & Export tab).

### Q: Can I sync between devices?
**A:** Not automatically. But you can:
1. Export data on Device A
2. Transfer the JSON file to Device B (email, USB, cloud storage)
3. Import data on Device B

### Q: Is my data private?
**A:** Yes! 100% private. Nothing is sent online, no tracking, no accounts needed.

---

## 🃏 Creating Cards

### Q: Can I add images to cards?
**A:** Yes! You can add images to both the front and back of cards. The IndexedDB version supports unlimited images.

### Q: What image formats are supported?
**A:** JPG, PNG, GIF, and WEBP formats are all supported.

### Q: How large can my images be?
**A:** Any size works, but 1-2MB per image is optimal for performance. The app will display them at appropriate sizes.

### Q: Can I add videos or audio?
**A:** Not currently. The app supports text and images only. Audio/video support is planned for future versions.

### Q: Do I need both text and images?
**A:** No! You can create cards with:
- Text only (front and back)
- Images only (front and back)
- Any combination (text on front, image on back, etc.)
- As long as both sides have *something* (text or image)

### Q: Can I edit cards after creating them?
**A:** Yes! Click "View Cards" on any deck, then click "Edit" on the card you want to change.

### Q: How do I delete a card?
**A:** Go to "View Cards" → Click "Delete" on the card → Confirm deletion.

---

## 📚 Decks & Organization

### Q: How many decks can I create?
**A:** Unlimited! Create as many decks as you need.

### Q: How many cards can be in one deck?
**A:** Unlimited! Some users have successfully created decks with 1,000+ cards.

### Q: Can I rename a deck?
**A:** Yes! Click "Edit" on any deck to change its name or description.

### Q: Can I move cards between decks?
**A:** Not directly in the UI. You would need to:
1. Export your data
2. Edit the JSON file to change card's deckId
3. Import the modified data

### Q: Can I organize decks into folders?
**A:** Not currently. All decks are displayed in one list. Consider using naming conventions like "Spanish - Verbs", "Spanish - Nouns", etc.

---

## 📖 Studying

### Q: What do the difficulty ratings mean?
**A:**
- **😓 Again** - Didn't know it. Card appears 3 more times.
- **🤔 Hard** - Struggled. Card appears 2 more times.
- **👍 Good** - Got it with effort. Card appears 1 more time.
- **✅ Easy** - Knew it instantly. Card is removed from this session.

### Q: Are cards shuffled during study?
**A:** Yes! Cards are randomized at the start of each study session.

### Q: Can I study specific cards?
**A:** Not currently. When you start a study session, all cards in the deck are included and shuffled.

### Q: What happens when I finish a study session?
**A:** You'll see a completion screen with your statistics, and the deck's study count increases.

### Q: Can I pause a study session?
**A:** Yes! Click "Exit Study" at any time. Your progress will be saved and the deck's study count will increase.

### Q: Why do some cards keep appearing?
**A:** If you rate a card as "Again", "Hard", or "Good", it gets added back to the study queue. Only "Easy" removes it from the current session.

### Q: Is there a time limit for studying?
**A:** No! Study at your own pace. Take breaks whenever you need.

---

## 📊 Statistics & Progress

### Q: What statistics are tracked?
**A:**
- Total decks created
- Total cards created
- Study sessions completed
- Cards mastered (in last session)

### Q: Can I see my study history over time?
**A:** Not currently. The app shows current statistics only. Detailed analytics are planned for future versions.

### Q: What counts as "Cards Mastered"?
**A:** Cards that you rated as "Easy" in your most recent study session.

---

## 💾 Backup & Export

### Q: How do I backup my data?
**A:**
1. Go to "Backup & Export" tab
2. Click "Export All Data"
3. Save the JSON file to a safe location (cloud storage, external drive, etc.)

### Q: How often should I backup?
**A:** We recommend weekly backups, or after creating significant new content.

### Q: What's included in the export?
**A:** Everything!
- All decks (names, descriptions, statistics)
- All cards (text content)
- All images (converted to base64)

### Q: How large will my backup file be?
**A:** It depends on how many images you have:
- Text-only data: Very small (few KB to few MB)
- With images: Can be large (10MB to 100MB+)

### Q: Can I edit the exported JSON file?
**A:** Yes, if you're comfortable with JSON format. See TECHNICAL.md for the data structure.

### Q: Can I import data from other flashcard apps?
**A:** Only if you convert their format to match our JSON structure. See TECHNICAL.md for details.

---

## 🔧 Troubleshooting

### Q: The app won't open / shows blank page
**A:** Try:
1. Use a different browser
2. Clear browser cache
3. Re-download the HTML file
4. Check if JavaScript is enabled in browser settings

### Q: "Error initializing database" message
**A:** Your browser might not support IndexedDB:
1. Update your browser to the latest version
2. Try Chrome/Firefox (best support)
3. Check if IndexedDB is enabled in settings

### Q: Images aren't displaying
**A:** Try:
1. Check if the image format is supported (JPG, PNG, GIF, WEBP)
2. Try a different, smaller image
3. Clear browser cache and reload
4. Export your data, clear all data, and re-import

### Q: Cards not saving
**A:** Make sure:
1. You added content to BOTH front and back
2. Browser has storage permission
3. You have available disk space
4. JavaScript is enabled

### Q: "Quota exceeded" error
**A:**
1. Check available disk space on your computer
2. Export and delete old decks you don't need
3. Compress large images before uploading
4. Try using the app in a different browser

### Q: App is running slow
**A:** Try:
1. Close other browser tabs
2. Restart your browser
3. Clear browser cache
4. Reduce image sizes (compress before uploading)

### Q: Lost all my data!
**A:**
1. Check if you're using the same browser
2. Don't clear browser data/cookies
3. Restore from your last backup (if available)
4. Check browser settings for site data

---

## 🔄 Migration & Compatibility

### Q: Can I use both localStorage and IndexedDB versions?
**A:** Yes, but they store data separately. They won't share decks.

### Q: Which version should I use?
**A:**
- **Use IndexedDB version** if you have lots of images
- **Use localStorage version** if you only have text (simpler, but has limits)

### Q: How do I migrate from localStorage to IndexedDB?
**A:** Unfortunately, automatic migration isn't available. You'll need to:
1. Export from localStorage version (browser console method)
2. Manually convert the format
3. Import into IndexedDB version

Or simply recreate your decks in the new version.

---

## 📱 Mobile-Specific Questions

### Q: Can I add the app to my home screen?
**A:**
- **iOS**: Open in Safari → Share → Add to Home Screen
- **Android**: Open in Chrome → Menu (⋮) → Add to Home Screen

### Q: Why is mobile storage limited?
**A:** Mobile browsers have stricter limits for security/performance. Typically 50MB-500MB depending on device.

### Q: Can I use it offline on mobile?
**A:** Yes! After opening once, it works fully offline.

---

## 🆕 Feature Requests

### Q: Can you add [feature X]?
**A:** The app is designed to be simple and self-contained. However, you can:
1. Modify the HTML file yourself (it's open source!)
2. Check TECHNICAL.md for customization guides
3. Check CHANGELOG.md for planned features

### Q: Will there be a native app?
**A:** Not currently planned. The web version works on all devices.

### Q: Can you add cloud sync?
**A:** Not planned, as it would require a server and reduce privacy. Use Export/Import for manual sync.

---

## 💡 Best Practices

### Q: How many cards should I study per day?
**A:** Start with 10-20 new cards per day. Adjust based on your capacity and retention.

### Q: What's the best way to create cards?
**A:**
- Keep it simple (one concept per card)
- Use images when possible
- Be specific, not vague
- Add context if needed
- Review and update unclear cards

### Q: Should I create reverse cards?
**A:** Yes, for language learning and definitions! Create two cards:
- Card 1: "English word" → "Spanish word"
- Card 2: "Spanish word" → "English word"

### Q: How long should study sessions be?
**A:** 10-20 minutes is ideal for focus and retention. Multiple short sessions beat one long session!

---

## 🔐 Security & Privacy

### Q: Is the app safe to use?
**A:** Yes! It's just HTML, CSS, and JavaScript. No malicious code. You can inspect the code yourself.

### Q: Do you collect any data?
**A:** No! Zero data collection, no analytics, no tracking. Everything stays on your device.

### Q: Can others access my cards?
**A:** Only if they have physical access to your computer and browser. Use your computer's user account security.

### Q: Should I password-protect the app?
**A:** The app doesn't have built-in password protection. Use your operating system's user account password/lock instead.

---

## 🎓 Learning & Study Tips

### Q: How long until I see results?
**A:** Depends on the subject and your effort! Generally:
- Basic vocabulary: 2-4 weeks
- Complex subjects: 2-3 months
- Mastery: 6-12 months with daily practice

### Q: What if I keep forgetting cards?
**A:** Normal! That's why they repeat. Tips:
- Rate yourself honestly
- Add more context or images
- Study daily (consistency matters)
- Break complex cards into simpler ones

### Q: Should I study multiple decks at once?
**A:** Yes, mixing subjects can improve retention. But don't overwhelm yourself!

---

## 🔮 Future Features

### Q: What's coming next?
**A:** See CHANGELOG.md for planned features:
- Spaced repetition algorithm
- Dark mode
- Tag system
- Enhanced statistics
- Audio support

---

## 📞 Getting Help

### Q: Where can I get help?
**A:**
1. Check this FAQ
2. Read README.md for detailed info
3. Read TECHNICAL.md for advanced help
4. Check browser console (F12) for error messages

### Q: How do I report a bug?
**A:** Document the issue with:
- What browser you're using
- What you were doing when it happened
- Any error messages in the console (F12)
- Steps to reproduce the problem

---

**Still have questions? Check out README.md and TECHNICAL.md for more detailed information!** 📚