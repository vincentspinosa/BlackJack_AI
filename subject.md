The software has to be a Blackjack AI, which comes in the form of a solver that can be opened in a web browser, and with the following features:

# Game Setup
- **Player Configuration**
  - Number of player seats (1-7)
  - Seat selection (which seats are occupied)
  - Individual or uniform bankroll settings

- **Deck Configuration**
  - Number of decks (1-8)
  - Cut card penetration percentage (50-95%)
  - Automatic shuffle detection

- **Rule Customization**
  - Surrender type: None, Late Surrender, Early Surrender
  - Dealer soft 17: Stand (S17) or Hit (H17)
  - Double After Split (DAS): Enabled/Disabled
  - Resplit Aces: Enabled/Disabled
  - Hit Split Aces: Enabled/Disabled
  - Blackjack payout: 3:2 or 6:5
  - Minimum bet amount
  - Maximum bet amount (optional, no limit)

- **AI Configuration**
  - Monte Carlo simulation, with Hi-lo card counting, Basic Strategy and Deviations
  - Balance between accuracy and performance

# Gameplay Features

- **Card Dealing**
  - Manual card input via clickable card picker
  - Visual feedback for available cards
  - Card count tracking per rank
  - Disabled state for depleted ranks

- **Betting Phase**
  - AI-recommended bet sizing based on true count
  - Bet ramp: 1x, 2x, 4x, 6x, 8x units based on count

- **Player Actions**
  - Hit: Receive additional card
  - Stand: End turn with current hand
  - Double: Double bet, receive one card
  - Split: Split pairs into two hands
  - Surrender: Forfeit half bet (if allowed)

- **Hand Management**
  - Multiple hands possible per player (when a player splits)
  - Hand selection and switching
  - Visual indication of active hand
  - Hand status tracking (active, stand, bust, blackjack, surrendered)

- **Dealer Actions**
  - Automatic dealer play according to rules
  - Soft 17 handling (S17/H17)
  - Dealer blackjack detection
  - Bust detection

# AI Features

- **Strategy Recommendations**
  - Optimal move recommendation (Hit/Stand/Double/Split/Surrender)
  - Expected Value (EV) calculation for all legal actions
  - Real-time updates based on current game state
  - Visual display of recommendation and EV breakdown

- **Card Counting**
  - Running count tracking
  - True count calculation (running count / decks remaining)
  - Number of cards remaining in shoe
  - Penetration percentage display
  - Automatic count updates on card input

- **Insurance Decisions**
  - Insurance recommendation when dealer shows Ace
  - Probability-based calculation using remaining shoe composition

- **Bet Sizing**
  - True count-based bet recommendations
  - Stepped bet ramp (1-8 units)

# Advanced Features

- **State Management**
  - Undo functionality, reinitialized each hand
  - History tracking

- **Player Management**
  - Add players
  - Remove players
  - Automatic bankroll updates
  - Automatic player removal on bankroll depletion
