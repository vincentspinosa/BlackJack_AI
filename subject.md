# Expected Features

The software has to be a Blackjack AI, which comes in the form of a solver that can be opened in a web browser, and with the following features:

## Core Game Features

### Game Setup
- **Player Configuration**
  - Number of player seats (1-7)
  - Seat selection (which seats are occupied)
  - Individual or uniform bankroll settings
  - Initial bankroll per player/seat

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
  - Monte Carlo simulation sample size (200-10,000)
  - Balance between accuracy and performance

### Gameplay Features

- **Card Dealing**
  - Manual card input via clickable card picker
  - Visual feedback for available cards
  - Card count tracking per rank
  - Disabled state for depleted ranks

- **Betting Phase**
  - AI-recommended bet sizing based on true count
  - Bet ramp: 1x, 2x, 4x, 6x, 8x units based on count
  - Bankroll constraints and management
  - Visual bet recommendations per player

- **Player Actions**
  - Hit: Receive additional card
  - Stand: End turn with current hand
  - Double Down: Double bet, receive one card
  - Split: Split pairs into two hands
  - Surrender: Forfeit half bet (if allowed)

- **Hand Management**
  - Multiple hands per player (up to 4 hands)
  - Hand selection and switching
  - Visual indication of active hand
  - Hand status tracking (active, stand, bust, blackjack, surrendered)

- **Dealer Actions**
  - Automatic dealer play according to rules
  - Soft 17 handling (S17/H17)
  - Dealer blackjack detection
  - Bust detection

### AI Features

- **Strategy Recommendations**
  - Optimal move recommendation (Hit/Stand/Double/Split/Surrender)
  - Expected Value (EV) calculation for all legal actions
  - Real-time updates based on current game state
  - Visual display of recommendation and EV breakdown

- **Card Counting**
  - Running count tracking
  - True count calculation (running count / decks remaining)
  - Cards remaining in shoe
  - Penetration percentage display
  - Automatic count updates on card input

- **Insurance Decisions**
  - Insurance recommendation when dealer shows Ace
  - Probability-based calculation using remaining shoe composition
  - Clear visual prompt with recommendation

- **Bet Sizing**
  - True count-based bet recommendations
  - Stepped bet ramp (1-8 units)
  - Bankroll percentage caps (max 25% per bet)
  - Minimum bet enforcement

### Advanced Features

- **State Management**
  - Undo functionality (cancel previous action)
  - State snapshot system
  - Action history tracking

- **Player Management**
  - Add players mid-game (empty seats)
  - Remove players (between hands)
  - Bankroll updates during settlement phase
  - Automatic player removal on bankroll depletion

- **Game Flow**
  - Hand-by-hand progression
  - Settlement phase with payout calculation
  - Next hand initialization
  - Shuffle detection and automatic reset

## User Interface Features

### Layout
- **Three-Column Grid Layout**
  - Left column: Game info and player areas
  - Center column: Dealer area, AI recommendations, user actions
  - Right column: Card picker and controls

### User Experience
- **Clear Prompts**: Text instructions for each game phase
- **Visual Feedback**: Hover effects, disabled states, active states
- **Error Prevention**: Disabled buttons for invalid actions
- **Information Display**: Running count, true count, cards remaining, penetration

## Technical Features

### Performance
- **Efficient Simulation**: Optimized Monte Carlo algorithm
- **Fast UI Updates**: Minimal DOM manipulation
- **Memory Management**: Efficient state handling
- **Smooth Interactions**: Responsive button clicks and card selection

### Reliability
- **Error Handling**: Graceful handling of edge cases
- **State Validation**: Consistency checks throughout game flow
- **Input Validation**: Sanitized user inputs
- **Boundary Checks**: Prevents invalid game states
